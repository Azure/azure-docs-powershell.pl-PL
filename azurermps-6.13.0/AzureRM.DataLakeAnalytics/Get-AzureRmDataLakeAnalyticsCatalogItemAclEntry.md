---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718340"
---
# <span data-ttu-id="b6b98-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b6b98-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="b6b98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6b98-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b98-103">Pobiera wpis z listy ACL wykazu lub elementu wykazu w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6b98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6b98-104">SYNTAX</span></span>

### <span data-ttu-id="b6b98-105">GetCatalogAclEntry (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b6b98-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6b98-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="b6b98-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6b98-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="b6b98-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6b98-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b6b98-108">GetCatalogItemAclEntry</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6b98-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="b6b98-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6b98-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="b6b98-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6b98-111">Opis</span><span class="sxs-lookup"><span data-stu-id="b6b98-111">DESCRIPTION</span></span>
<span data-ttu-id="b6b98-112">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** pobiera listę wpisów (ACE) na liście kontroli dostępu (ACL) wykazu lub elementu wykazu w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-112">The **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="b6b98-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6b98-113">EXAMPLES</span></span>

### <span data-ttu-id="b6b98-114">Przykład 1: Pobieranie listy ACL dla wykazu</span><span class="sxs-lookup"><span data-stu-id="b6b98-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="b6b98-115">To polecenie pobiera listę ACL dla wykazu określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="b6b98-116">Przykład 2: pobieranie wpisu ACL właściciela użytkownika dla wykazu</span><span class="sxs-lookup"><span data-stu-id="b6b98-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="b6b98-117">To polecenie pobiera wpis listy ACL właściciela użytkownika dla wykazu określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="b6b98-118">Przykład 3: pobieranie wpisu ACL dla właściciela grupy dla wykazu</span><span class="sxs-lookup"><span data-stu-id="b6b98-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="b6b98-119">To polecenie pobiera wpis listy ACL właściciela grupy dla wykazu określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="b6b98-120">Przykład 4: Pobieranie listy ACL dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="b6b98-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="b6b98-121">To polecenie pobiera listę ACL dla bazy danych określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="b6b98-122">Przykład 5: pobieranie wpisu ACL dla właściciela bazy danych dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="b6b98-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="b6b98-123">To polecenie pobiera wpis listy ACL właściciela użytkownika dla bazy danych określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="b6b98-124">Przykład 6: pobieranie wpisu ACL dla właściciela grupy dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="b6b98-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="b6b98-125">To polecenie pobiera wpis ACL właściciela grupy dla bazy danych określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="b6b98-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6b98-126">PARAMETERS</span></span>

### <span data-ttu-id="b6b98-127">— Konto</span><span class="sxs-lookup"><span data-stu-id="b6b98-127">-Account</span></span>
<span data-ttu-id="b6b98-128">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6b98-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b6b98-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b98-129">-DefaultProfile</span></span>
<span data-ttu-id="b6b98-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b98-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6b98-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="b6b98-131">-GroupOwner</span></span>
<span data-ttu-id="b6b98-132">Pobieranie wpisu ACL wykazu dla właściciela grupy</span><span class="sxs-lookup"><span data-stu-id="b6b98-132">Get ACL entry of catalog for group owner</span></span>

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

### <span data-ttu-id="b6b98-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b6b98-133">-ItemType</span></span>
<span data-ttu-id="b6b98-134">Określa typ elementów wykazu lub katalogów.</span><span class="sxs-lookup"><span data-stu-id="b6b98-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="b6b98-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6b98-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6b98-136">Wykazu</span><span class="sxs-lookup"><span data-stu-id="b6b98-136">Catalog</span></span>
- <span data-ttu-id="b6b98-137">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="b6b98-137">Database</span></span>

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

### <span data-ttu-id="b6b98-138">-Path</span><span class="sxs-lookup"><span data-stu-id="b6b98-138">-Path</span></span>
<span data-ttu-id="b6b98-139">Określa ścieżkę usługi Data Lake Analytics wykazu lub elementu wykazu.</span><span class="sxs-lookup"><span data-stu-id="b6b98-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="b6b98-140">Części ścieżki powinny być oddzielone kropką (.).</span><span class="sxs-lookup"><span data-stu-id="b6b98-140">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="b6b98-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="b6b98-141">-UserOwner</span></span>
<span data-ttu-id="b6b98-142">Pobieranie wpisu ACL wykazu dla właściciela użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6b98-142">Get ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="b6b98-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b98-143">CommonParameters</span></span>
<span data-ttu-id="b6b98-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b98-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b98-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b98-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b98-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6b98-146">INPUTS</span></span>

### <span data-ttu-id="b6b98-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b6b98-147">System.String</span></span>

### <span data-ttu-id="b6b98-148">Microsoft. Azure. Commands. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="b6b98-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="b6b98-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6b98-149">OUTPUTS</span></span>

### <span data-ttu-id="b6b98-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="b6b98-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="b6b98-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6b98-151">NOTES</span></span>

## <span data-ttu-id="b6b98-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6b98-152">RELATED LINKS</span></span>

[<span data-ttu-id="b6b98-153">Pozycja U — SQL oferuje teraz kontrolę dostępu na poziomie bazy danych</span><span class="sxs-lookup"><span data-stu-id="b6b98-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="b6b98-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b6b98-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="b6b98-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b6b98-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
