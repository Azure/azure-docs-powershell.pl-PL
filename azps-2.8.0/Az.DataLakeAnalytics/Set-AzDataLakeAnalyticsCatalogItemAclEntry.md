---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 4187addb4a256e3304ea5fc8a7bdfb19ed71ac46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705857"
---
# <span data-ttu-id="d8571-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d8571-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="d8571-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8571-102">SYNOPSIS</span></span>
<span data-ttu-id="d8571-103">Modyfikuje wpis na liście ACL wykazu lub elementu wykazu w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8571-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d8571-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8571-104">SYNTAX</span></span>

### <span data-ttu-id="d8571-105">SetCatalogAclEntryForUser (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d8571-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8571-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="d8571-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8571-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d8571-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8571-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d8571-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8571-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="d8571-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8571-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="d8571-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8571-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="d8571-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8571-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="d8571-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8571-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="d8571-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8571-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="d8571-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8571-115">Opis</span><span class="sxs-lookup"><span data-stu-id="d8571-115">DESCRIPTION</span></span>
<span data-ttu-id="d8571-116">Polecenie cmdlet **Set-AzDataLakeAnalyticsCatalogItemAclEntry** dodaje lub modyfikuje wpis (ACE) na liście kontroli dostępu (ACL) wykazu lub elementu wykazu w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8571-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d8571-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8571-117">EXAMPLES</span></span>

### <span data-ttu-id="d8571-118">Przykład 1: Modyfikowanie uprawnień użytkowników do wykazu</span><span class="sxs-lookup"><span data-stu-id="d8571-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d8571-119">To polecenie modyfikuje wpis ACE wykazu dla Patti, aby uzyskać uprawnienia do odczytu.</span><span class="sxs-lookup"><span data-stu-id="d8571-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="d8571-120">Przykład 2: Modyfikowanie uprawnień użytkowników do bazy danych</span><span class="sxs-lookup"><span data-stu-id="d8571-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d8571-121">To polecenie modyfikuje bazę danych ACE dla Patti, aby uzyskać uprawnienia do odczytu.</span><span class="sxs-lookup"><span data-stu-id="d8571-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="d8571-122">Przykład 3: modyfikowanie innych uprawnień do wykazu</span><span class="sxs-lookup"><span data-stu-id="d8571-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d8571-123">To polecenie modyfikuje wpis ACE wykazu, aby uzyskać uprawnienia do odczytu.</span><span class="sxs-lookup"><span data-stu-id="d8571-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="d8571-124">Przykład 4: modyfikowanie innych uprawnień do bazy danych</span><span class="sxs-lookup"><span data-stu-id="d8571-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="d8571-125">Przykład 5: Modyfikowanie uprawnień właściciela użytkownika dla wykazu</span><span class="sxs-lookup"><span data-stu-id="d8571-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="d8571-126">To polecenie ustawia uprawnienie właściciela konta do odczytu.</span><span class="sxs-lookup"><span data-stu-id="d8571-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="d8571-127">Przykład 6: Modyfikowanie uprawnień właociciela użytkownika dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="d8571-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="d8571-128">To polecenie ustawia uprawnienie właściciela bazy danych do odczytu.</span><span class="sxs-lookup"><span data-stu-id="d8571-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="d8571-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8571-129">PARAMETERS</span></span>

### <span data-ttu-id="d8571-130">— Konto</span><span class="sxs-lookup"><span data-stu-id="d8571-130">-Account</span></span>
<span data-ttu-id="d8571-131">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8571-131">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8571-132">-DefaultProfile</span></span>
<span data-ttu-id="d8571-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8571-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-134">-Group</span><span class="sxs-lookup"><span data-stu-id="d8571-134">-Group</span></span>
<span data-ttu-id="d8571-135">Ustawianie wpisu ACL wykazu dla grupy.</span><span class="sxs-lookup"><span data-stu-id="d8571-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="d8571-136">-GroupOwner</span></span>
<span data-ttu-id="d8571-137">Ustawianie wpisu ACL wykazu dla właściciela grupy.</span><span class="sxs-lookup"><span data-stu-id="d8571-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="d8571-138">-ItemType</span></span>
<span data-ttu-id="d8571-139">Określa typ elementów wykazu lub katalogów.</span><span class="sxs-lookup"><span data-stu-id="d8571-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="d8571-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d8571-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8571-141">Wykazu</span><span class="sxs-lookup"><span data-stu-id="d8571-141">Catalog</span></span>
- <span data-ttu-id="d8571-142">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="d8571-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d8571-143">-ObjectId</span></span>
<span data-ttu-id="d8571-144">Tożsamość użytkownika, który ma zostać ustawiony.</span><span class="sxs-lookup"><span data-stu-id="d8571-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-145">-Inne</span><span class="sxs-lookup"><span data-stu-id="d8571-145">-Other</span></span>
<span data-ttu-id="d8571-146">Ustawianie wpisu ACL wykazu innej listy.</span><span class="sxs-lookup"><span data-stu-id="d8571-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-147">-Path</span><span class="sxs-lookup"><span data-stu-id="d8571-147">-Path</span></span>
<span data-ttu-id="d8571-148">Określa ścieżkę usługi Data Lake Analytics wykazu lub elementu wykazu.</span><span class="sxs-lookup"><span data-stu-id="d8571-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="d8571-149">Części ścieżki powinny być oddzielone kropką (.).</span><span class="sxs-lookup"><span data-stu-id="d8571-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-150">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="d8571-150">-Permissions</span></span>
<span data-ttu-id="d8571-151">Określa uprawnienia wpisu ACE.</span><span class="sxs-lookup"><span data-stu-id="d8571-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="d8571-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d8571-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8571-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d8571-153">None</span></span>
- <span data-ttu-id="d8571-154">Czytał</span><span class="sxs-lookup"><span data-stu-id="d8571-154">Read</span></span>
- <span data-ttu-id="d8571-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d8571-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-156">-User</span><span class="sxs-lookup"><span data-stu-id="d8571-156">-User</span></span>
<span data-ttu-id="d8571-157">Ustawianie wpisu ACL wykazu dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d8571-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="d8571-158">-UserOwner</span></span>
<span data-ttu-id="d8571-159">Ustawianie wpisu ACL wykazu dla właściciela użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d8571-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8571-160">-Confirm</span></span>
<span data-ttu-id="d8571-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8571-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8571-162">-WhatIf</span></span>
<span data-ttu-id="d8571-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8571-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8571-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8571-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8571-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8571-165">CommonParameters</span></span>
<span data-ttu-id="d8571-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8571-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8571-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8571-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8571-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8571-168">INPUTS</span></span>

### <span data-ttu-id="d8571-169">System. String</span><span class="sxs-lookup"><span data-stu-id="d8571-169">System.String</span></span>

### <span data-ttu-id="d8571-170">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d8571-170">System.Guid</span></span>

### <span data-ttu-id="d8571-171">Microsoft. Azure. Commands. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="d8571-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="d8571-172">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsEnums + uprawnienie</span><span class="sxs-lookup"><span data-stu-id="d8571-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="d8571-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8571-173">OUTPUTS</span></span>

### <span data-ttu-id="d8571-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="d8571-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="d8571-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8571-175">NOTES</span></span>

## <span data-ttu-id="d8571-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8571-176">RELATED LINKS</span></span>

[<span data-ttu-id="d8571-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d8571-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="d8571-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d8571-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="d8571-179">Pozycja U — SQL oferuje teraz kontrolę dostępu na poziomie bazy danych</span><span class="sxs-lookup"><span data-stu-id="d8571-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
