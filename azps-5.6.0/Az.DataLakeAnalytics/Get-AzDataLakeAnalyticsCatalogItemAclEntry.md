---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 63e0f3622ea7ae83f805688e4634b30c38cb601d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964769"
---
# <span data-ttu-id="45e6e-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="45e6e-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="45e6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="45e6e-103">Pobiera wpis do listy ACL wykazu lub elementu wykazu w narzędziu Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45e6e-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="45e6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45e6e-104">SYNTAX</span></span>

### <span data-ttu-id="45e6e-105">GetCatalogAclEntry (domyślne)</span><span class="sxs-lookup"><span data-stu-id="45e6e-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45e6e-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="45e6e-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45e6e-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="45e6e-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45e6e-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="45e6e-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45e6e-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="45e6e-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45e6e-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="45e6e-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45e6e-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="45e6e-111">DESCRIPTION</span></span>
<span data-ttu-id="45e6e-112">Polecenie **cmdlet Get-AzDataLakeAnalyticsCatalogItemAclEntry** pobiera listę pozycji ( ACEs) na liście kontroli dostępu (ACL, Access Control List) wykazu lub elementu wykazu w narzędziu Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45e6e-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="45e6e-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45e6e-113">EXAMPLES</span></span>

### <span data-ttu-id="45e6e-114">Przykład 1. Uzyskiwanie listy ACL dla wykazu</span><span class="sxs-lookup"><span data-stu-id="45e6e-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="45e6e-115">To polecenie pobiera wartość ACL dla wykazu określonego konta Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="45e6e-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="45e6e-116">Przykład 2. Uzyskiwanie wpisu listy ACL właściciela katalogu</span><span class="sxs-lookup"><span data-stu-id="45e6e-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="45e6e-117">To polecenie pobiera wpis ACL właściciela użytkownika w wykazie określonego konta Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="45e6e-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="45e6e-118">Przykład 3. Uzyskiwanie wpisu ACL właściciela grupy dla wykazu</span><span class="sxs-lookup"><span data-stu-id="45e6e-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="45e6e-119">To polecenie pobiera wpis ACL właściciela grupy dla katalogu określonego konta Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="45e6e-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="45e6e-120">Przykład 4. Uzyskiwanie listy ACL dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="45e6e-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="45e6e-121">To polecenie pobiera wartość ACL dla bazy danych określonego konta Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="45e6e-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="45e6e-122">Przykład 5. Uzyskiwanie wpisu ACL właściciela bazy danych</span><span class="sxs-lookup"><span data-stu-id="45e6e-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="45e6e-123">To polecenie pobiera wpis ACL właściciela użytkownika dla bazy danych określonego konta Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="45e6e-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="45e6e-124">Przykład 6. Uzyskiwanie wpisu ACL właściciela grupy bazy danych</span><span class="sxs-lookup"><span data-stu-id="45e6e-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="45e6e-125">To polecenie pobiera wpis ACL właściciela grupy dla bazy danych określonego konta Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="45e6e-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="45e6e-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45e6e-126">PARAMETERS</span></span>

### <span data-ttu-id="45e6e-127">— Konto</span><span class="sxs-lookup"><span data-stu-id="45e6e-127">-Account</span></span>
<span data-ttu-id="45e6e-128">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="45e6e-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="45e6e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e6e-129">-DefaultProfile</span></span>
<span data-ttu-id="45e6e-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45e6e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45e6e-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="45e6e-131">-GroupOwner</span></span>
<span data-ttu-id="45e6e-132">Uzyskiwanie wpisu listy ACL wykazu dla właściciela grupy</span><span class="sxs-lookup"><span data-stu-id="45e6e-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6e-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="45e6e-133">-ItemType</span></span>
<span data-ttu-id="45e6e-134">Określa typ wykazu lub elementów wykazu.</span><span class="sxs-lookup"><span data-stu-id="45e6e-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="45e6e-135">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45e6e-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45e6e-136">Wykaz</span><span class="sxs-lookup"><span data-stu-id="45e6e-136">Catalog</span></span>
- <span data-ttu-id="45e6e-137">Baza danych</span><span class="sxs-lookup"><span data-stu-id="45e6e-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e6e-138">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="45e6e-138">-Path</span></span>
<span data-ttu-id="45e6e-139">Określa ścieżkę usługi Data Lake Analytics wykazu lub elementu wykazu.</span><span class="sxs-lookup"><span data-stu-id="45e6e-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="45e6e-140">Części ścieżki powinny być oddzielone kropka (.).</span><span class="sxs-lookup"><span data-stu-id="45e6e-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e6e-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="45e6e-141">-UserOwner</span></span>
<span data-ttu-id="45e6e-142">Uzyskaj wpis listy ACL wykazu dla właściciela użytkownika.</span><span class="sxs-lookup"><span data-stu-id="45e6e-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e6e-143">CommonParameters</span></span>
<span data-ttu-id="45e6e-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e6e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e6e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e6e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e6e-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45e6e-146">INPUTS</span></span>

### <span data-ttu-id="45e6e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="45e6e-147">System.String</span></span>

### <span data-ttu-id="45e6e-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="45e6e-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="45e6e-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45e6e-149">OUTPUTS</span></span>

### <span data-ttu-id="45e6e-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="45e6e-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="45e6e-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45e6e-151">NOTES</span></span>

## <span data-ttu-id="45e6e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45e6e-152">RELATED LINKS</span></span>

[<span data-ttu-id="45e6e-153">Język U-SQL oferuje teraz kontrolę dostępu na poziomie bazy danych</span><span class="sxs-lookup"><span data-stu-id="45e6e-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="45e6e-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="45e6e-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="45e6e-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="45e6e-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
