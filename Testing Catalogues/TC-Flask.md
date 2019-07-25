# TESTING-CATALOGUE Flask-Repository
This file contains a checklist of directories and modules in the `openease_flask`-repository which still need to be tested. We will rank them on a scale from ![one][one_16] to ![five][five_16] for the degree of difficulty for testing.

Please add the ![green_check][green_check_16] icon behind every module that has been tested, and the ![black_check][black_check_16] icon behind every tested method. If a module or method does not need testing, we mark it with a ![stop][stop_16] icon.  
(You can use test-coverage data to decide whether a method or module was tested enough.)

If a module is refactored, please consider indicating the changes in this file.

- ![folder][folder_16] **Webrob**
    - ![folder][folder_16] **config**
        - ![python][python_16] settings.py ![stop][stop_16]
    - ![folder][folder_16] **docker**
        - ![python][python_16] docker_application.py
            - **TODO**
        - ![python][python_16] docker_interface.py
            - **TODO**
    - ![folder][folder_16] **models**
        - ![python][python_16] db.py
            - `db_columns(cls)`
            - `db_column_names(cls)`
            - `db_find_all(cls)`
            - `db_find(cls, i)`
            - `db_find_name(cls, name)`
            - `db_update(cls, i, data)`
            - `db_create(cls, data)`
            - `db_remove(cls, i)`
            - `db_table_class(table_name)`
        - ![python][python_16] experiments.py ![stop][stop_16]
        - ![python][python_16] teaching.py
            - `find_courses(course)`
            - `get_exercises(course_id)`
            - `get_tasks(course_id)`
            - `get_task(exercise_id, task_number)`
        - ![python][python_16] tutorials.py
            - `read_tutorial_page(cat, page)`
        - ![python][python_16] users.py ![stop][stop_16]
    - ![folder][folder_16] **pages**
        - ![python][python_16] api.py
            - `login_by_session()`
            - `_generate_rosauth(user_container_name, dest, cache=False)`
            - `refresh_by_session()`
            - `login_by_token(token)`
            - `_user_by_token(token)`
            - `start_container(token)`
            - `_generate_user_image_name()`
            - `stop_container(token)`
            - `refresh_by_token(token)`
            - `create_api_token()`
            - `_create_token()`    
        - ![python][python_16] db.py
            - `db_docu_text(key)`
            - `_get_all_docs()`
            - `_display_warning_when_unable_to_find_docu(key)`
            - `db_page_user_roles()`
            - `db_find_user_roles()`
            - `_get_all_users()`
            - `db_save_user_roles()`
            - `_save_roles_to_users_and_commit_to_db(data)`
            - `db_page_route(table)`
            - `db_find_route(table)`
            - `db_update_route(table)`
            - `db_create_route(table)`
            - `db_remove_route(table)`
        - ![python][python_16] editor.py
            - `handle_pkg_error(error)`
            - `render_editor(filename="")`
            - `create_new_pkg()`
            - `_check_pkg_name_and_raise_error_if_already_exists(pkg_name)`
            - `_check_template_path_and_raise_error_if_does_not_exist(path)`
            - `_transfer_pkg_to_user_container(pkg_name, template_path)`
            - `_build_container_path(large_file_transferer, name)`
            - `_copy_pkg_to_user_container_and_replace_keywords(pkg_name, pkg_path, template_path)`
            - `_log_unable_to_create_pkg_error()`
            - `delete_pkg(package_name=None)`
            - `_check_pkg_name_and_if_none_get_pkg_name_from_session(package_name)`
            - `_log_unable_to_delete_pkg_error()`
            - `set_pkg()`
            - `_get_pkg_tree()`
            - `_get_root_files_from_container(pkg_path)`
            - `pkg_list()`
            - `read_pkg()`
            - `_get_file_path(file_name)`
            - `_read_file_from_container(path)`
            - `_log_unable_to_read_file_error()`
            - `download_pkg()`
            - `_zip_dir_to_container_and_return_dest_path(large_file_transferer, dir_name, source_dir_from_container=None)`
            - `_zip_dir_to_dest(large_file_transferer, src, dest)`
            - `_zip_dir(src_path, path_prefix, zip_file_writer)`
            - `pkg_save_exercise()`
            - `_get_exercise_from_db()`
            - `_read_archive_and_save_in_db(db_adapter, exercise, zip_path)`
            - `_log_unable_to_save_exercise_error()`
            - `pkg_load_exercise()`
            - `_create_pkg_zip_and_unzip_in_filetransfer_folder(exercise, large_file_transferer, pkg_name)`
            - `_create_pkg_zip_in_filetransfer_folder(exercise, zip_path)`
            - `_unzip_file_to_filetransfer_folder(large_file_transferer, zip_src_path)`
            - `_copy_exercise_to_user_container(large_file_transferer, pkg_name)`
            - `_log_unable_to_load_exercise_error()`
            - `write_file_to_container()`
            - `_write_file_to_user_container(data, path)`
            - `_log_unable_to_write_file_error()`
            - `_delete_file_from_container()`
            - `_remove_file_from_user_container(path)`
            - `_log_unable_to_delete_file_error()`
        - ![python][python_16] experiments.py
            - `download_episode(category=None, exp=None)`
            - `upload_episode(category=None, exp=None)`
            - `download_episode_ftp(category=None, exp=None)`
            - `upload_episode_ftp(category=None, exp=None)`
            - `episode_set(category, episode)`
            - `admin_experiments()`
            - `episode_data(category, exp)`
            - `experiment_del(cat, exp)`
            - `experiment_move(cat, exp)`
            - `get_exp_meta_data()`
            - `get_experiment_download_url()`
            - `get_experiment_list()`
            - `get_experiment_path(category, exp)`
            - `get_episode_owl_file(episode_path)`
            - `get_episode_interval(owl_file_path)`
            - `get_experiment_episodes(category, exp)`
            - `create_queries_file(cat, exp)`
            - `experiment_create_directory(cat, exp)`
            - `experiment_load_queries(category, exp)`
            - `experiment_save_queries(category, exp, data)`
        - ![python][python_16] knowrob.py
            - `download_static(filename)`
            - `download_logged_image(filename)`
            - `transfer_logged_video(filename)`
            - `transfer_logged_memory(filename)`
            - `knowrob(category=None, exp=None)`
            - `video(category=None, exp=None)`
            - `__knowrob_page__(template, container_name, category=None, exp=None)`
            - `menu()`
            - `_generate_episode_choices_map_from_experiment_list()`
            - `reset_knowledge_base()`
            - `add_history_item()`
            - `get_history_item()`
            - `user_data()`
            - `admin_cookie()`
            - `log()`
            - `get_history_file()`
            - `unhandled_exception(e)`
        - ![python][python_16] login.py
            - `track_login(sender, user, **extra)`
            - `track_logout(sender, user, **extra)`
            - `show_user_data()`
            - `_add_random_username_and_container_name_to_session()`
            - `_get_user_roles()`
            - `_get_exp_category()`
            - `_get_exp_name()`
            - `openease_remote()`
        - ![python][python_16] meshes.py
            - `is_mesh_url_valid(url)`
            - `update_meshes()`
            - `_update_meshes_run()`
            - `_change_to_mesh_data_directory()`
            - `_update_mesh_repositories()`
            - `_update_if_svn_or_git_repository(repo)`
            - `_tool_is_svn_repository(tool)`
            - `_tool_is_git_repository(tool)`
            - `_update_meshes_in_repository(url, repo_dir, repo_update_cmd, repo_clone_cmd)`
            - `_repository_exists(repo_name)`
            - `_update_repository(repo_name, repo_dir, repo_update_cmd)`
            - `_clone_repository(repo_dir, repo_clone_cmd, url)`
            - `_convert_tif_images_to_png()`
            - `download_mesh(mesh)`
            - `_get_mesh_file(mesh)`
            - `_get_m_file_from_repos(mesh)`
            - `_get_m_file_from_root(mesh)`
            - `_log_download_fail_message(mesh)`
            - `_send_mesh_file(mesh_file)`
        - ![python][python_16] mongo.py
            - `admin_mongo()`
            - `_connect_to_mongo_db()`
            - `_get_db_and_file_info(mongo_db)`
            - `_build_mongo_db_name(category, experiment)`
            - `_get_db_info(db_name, mongo_db)`
            - `_get_formatted_db_stats(stats)`
            - `_get_file_info(cat, exp)`
            - `_get_episode_sizes_and_collections(cat, exp)`
            - `_get_episode_files(cat, exp)`
            - `_get_formatted_file_info(cat, collections, exp, size)`
            - `_get_episode_count(cat, exp)`
            - `admin_mongo_update(cat, exp)`
            - `_drop_old_db_content(db_name)`
            - `_mongo_import_json(db_name, collection, json_file)`
            - `_mongo_import_bson(db_name, collection, bson_file)`
        - ![python][python_16] oauth.py
            - `tokens_are_defined(tokens)`
            - `remote_app_registered(name)`
            - `remote_app_login(remote_app, authorized)`
            - `remote_app_authorized(response, oauth_token_key, get_user_information)`
            - `get_oauth_token()`
            - `facebook_login()`
            - `twitter_login()`
            - `google_login()`
            - `github_login()`
            - `github_authorized(response)`
            - `_get_user_name(login)`
            - `_get_user_mail(login, domain)`
            - `facebook_authorized(response)`
            - `twitter_authorized(response)`
            - `google_authorized(response)`
        - ![python][python_16] tutorials.py
            - `tutorials()`
            - `get_tutorial()`
            - `read_tutorial(cat_id, page)`
            - `find_course()`
            - `get_exercise_()`
            - `get_task_()`
            - `teaching()`
    - ![folder][folder_16] **startup**
        - ![python][python_16] init_app.py
            - `add_user(app, db, user_manager, name, mail, pw, display_name='', remote_app='', roles=[])`
            - `_check_password_and_display_message_on_error(app, name, pw)`
            - `_password_criteria_fulfilled(pw)`
            - `_has_six_or_more_chars(str)`
            - `_contains_number(str)`
            - `_contains_lowercase_letter(str)`
            - `_contains_uppercase_letter(str)`
            - `_get_user_from_db(name)`
            - `_create_new_user_and_add_to_db(app, db, user_manager, name, mail, pw, display_name, remote_app, roles)`
            - `_append_roles_to_user_object(app, user, roles)`
            - `_get_role_from_db(role)`
            - `_log_role_query_failure(app, role)`
            - `_add_user_to_db(app, db, user)`
            - `init_app(app, db_instance, extra_config_settings={})`
            - `_init_app_config_settings(app, extra_config_settings)`
            - `_log_webapp_started(app)`
        - ![python][python_16] init_db.py ![stop][stop_16]
        - ![python][python_16] init_webapp.py ![stop][stop_16]
    - ![folder][folder_16] **utility**
        - ![python][python_16] db_connection_checker.py
            - `got_db_connection(app, db)`
        - ![python][python_16] directory_handler.py
            - `mk_dir(path)`
            - `make_dirs(path)`
            - `rm_empty_dir(path)`
            - `rm_nonempty_dir(path)`
            - `ch_dir(path)`
            - `get_current_working_directory()`
            - `list_directories(path)`
            - `walk_directories(top, topdown=True, onerror=None, followlinks=False)`
        - ![python][python_16] file_handler.py
            - `read_file(path)`
            - `write_to_file(path, content)`
            - `create_file(path, content=None)`
            - `remove_file(path)`
        - ![python][python_16] path_handler.py
            - `join_paths(path, *paths)`
            - `path_exists(path)`
            - `absolute_path(path)`
            - `relative_path(path, start)`
            - `get_parent_dir_name(path)`
            - `get_path_basename(path)`
            - `get_unix_style_path_basename(path)`
            - `is_directory(path)`
            - `get_path_size(path)`
            - `split_path(path)`
            - `split_extension(path)`
        - ![python][python_16] random_string_builder.py
            - `random_string(length)`
        - ![python][python_16] system_environment_variable_getter.py
            - `get_required_variable(var_name)`
            - `get_variable_with_default(var_name, default)`
            - `get_variable_with_default_none(var_name)`
        - ![python][python_16] template_file_copyer.py
            - `copy_template_file_and_replace_keywords(src, dst, args)`
            - `_create_parent_dir(dst)`
            - `_copy_file_and_replace_keywords(dst, template, args)`
            - `_format_template(template, args)`
            - `_get_number_of_template_fillers(template)`
        - ![python][python_16] utility.py
            - `get_user_dir()`
            - `admin_required(f)`
    - ![python][python_16] app_and_db.py ![stop][stop_16]
- ![python][python_16] runserver.py
    - `_config_is_debug()`
    - `_run_debug_server()`
    - `_run_server()`
    - `__main__()`

**Icon References:**
- [![one][one_16] ![two][two_16] ![three][three_16] ![four][four_16] ![five][five_16]](https://www.flaticon.com/packs/characters-and-numbers) Icons made by [Twitter](https://www.flaticon.com/authors/twitter) from [www.flaticon.com]() are licensed under [CC 3.0 BY.](https://creativecommons.org/licenses/by/3.0/)
- [![stop][stop_16]](https://www.flaticon.com/free-icon/stop_151955#term=stop&page=1&position=18) Icons made by [Chanut](https://www.flaticon.com/authors/chanut) from [www.flaticon.com]() are licensed under [CC 3.0 BY.](https://creativecommons.org/licenses/by/3.0/)
- [![python][python_16]](https://www.flaticon.com/free-icon/python_919852#term=python&page=1&position=4) Icons made by [Freepik](https://www.flaticon.com/authors/freepik) from [www.flaticon.com]() are licensed under [CC 3.0 BY.](https://creativecommons.org/licenses/by/3.0/)
- [![folder][folder_16]](https://www.flaticon.com/free-icon/folder_148947#term=folder&page=1&position=36) Icons made by [SmashIcons](https://www.flaticon.com/authors/smashicons) from [www.flaticon.com]() are licensed under [CC 3.0 BY.](https://creativecommons.org/licenses/by/3.0/)
- [![green_check][green_check_16]](https://www.flaticon.com/free-icon/checked_291201#term=check&page=1&position=2) Icon made by [Maxim Basinski](https://www.flaticon.com/authors/maxim-basinski) from [www.flaticon.com]() is licensed under [CC 3.0 BY.](https://creativecommons.org/licenses/by/3.0/)
- [![black_check][black_check_16]](https://www.flaticon.com/free-icon/check-symbol_60731#term=check&page=1&position=19) Icon made by [Google](https://www.flaticon.com/authors/google)  from [www.flaticon.com]() is licensed under [CC 3.0 BY.](https://creativecommons.org/licenses/by/3.0/)

(Click the icons to be directed to the source page)

[one_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/Numbers/one_16.png
[two_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/Numbers/two_16.png
[three_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/Numbers/three_16.png
[four_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/Numbers/four_16.png
[five_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/Numbers/five16.png
[stop_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/stop_16.png
[python_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/python_16.png
[python_24]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/python_24.png
[folder_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/folder_16.png
[folder_24]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/folder_24.png
[green_check_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/green_check_16.png
[black_check_16]: https://raw.githubusercontent.com/navidJadid/openease_webserver_development/master/Testing%20Catalogues/Icons/black_check_16.png