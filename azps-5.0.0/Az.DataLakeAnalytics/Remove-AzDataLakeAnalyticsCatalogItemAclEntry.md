---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 8b227d16a55d1e5f92c6021099a01b9df5550bd2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305802"
---
# <span data-ttu-id="2eb36-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2eb36-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="2eb36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eb36-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb36-103">Usuwa wpis z listy ACL wykazu lub elementu wykazu w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2eb36-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="2eb36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eb36-104">SYNTAX</span></span>

### <span data-ttu-id="2eb36-105">RemoveCatalogAclEntryForUser (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2eb36-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb36-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="2eb36-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2eb36-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="2eb36-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb36-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="2eb36-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2eb36-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2eb36-109">DESCRIPTION</span></span>
<span data-ttu-id="2eb36-110">Polecenie cmdlet **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** usuwa wpis (ACE) z listy kontroli dostępu (ACL) wykazu lub elementu wykazu w usłudze Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2eb36-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="2eb36-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eb36-111">EXAMPLES</span></span>

### <span data-ttu-id="2eb36-112">Przykład 1: Usuwanie listy ACL użytkowników dla wykazu</span><span class="sxs-lookup"><span data-stu-id="2eb36-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="2eb36-113">To polecenie usuwa wykaz ACL wykazu dla Patti w pełni na koncie contosoadla.</span><span class="sxs-lookup"><span data-stu-id="2eb36-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="2eb36-114">Przykład 2: Usuwanie listy ACL użytkowników dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="2eb36-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="2eb36-115">To polecenie usuwa listę ACL bazy danych dla Pattigo pełnego contosoadla konta.</span><span class="sxs-lookup"><span data-stu-id="2eb36-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="2eb36-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eb36-116">PARAMETERS</span></span>

### <span data-ttu-id="2eb36-117">— Konto</span><span class="sxs-lookup"><span data-stu-id="2eb36-117">-Account</span></span>
<span data-ttu-id="2eb36-118">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2eb36-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2eb36-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb36-119">-DefaultProfile</span></span>
<span data-ttu-id="2eb36-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb36-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb36-121">-Group</span><span class="sxs-lookup"><span data-stu-id="2eb36-121">-Group</span></span>
<span data-ttu-id="2eb36-122">Usuwanie wpisu ACL wykazu dla grupy.</span><span class="sxs-lookup"><span data-stu-id="2eb36-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb36-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="2eb36-123">-ItemType</span></span>
<span data-ttu-id="2eb36-124">Określa typ elementów wykazu lub katalogów.</span><span class="sxs-lookup"><span data-stu-id="2eb36-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="2eb36-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2eb36-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2eb36-126">Wykazu</span><span class="sxs-lookup"><span data-stu-id="2eb36-126">Catalog</span></span>
- <span data-ttu-id="2eb36-127">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="2eb36-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb36-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2eb36-128">-ObjectId</span></span>
<span data-ttu-id="2eb36-129">Tożsamość użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="2eb36-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb36-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eb36-130">-PassThru</span></span>
<span data-ttu-id="2eb36-131">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="2eb36-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb36-132">-Path</span><span class="sxs-lookup"><span data-stu-id="2eb36-132">-Path</span></span>
<span data-ttu-id="2eb36-133">Określa ścieżkę usługi Data Lake Analytics wykazu lub elementu wykazu.</span><span class="sxs-lookup"><span data-stu-id="2eb36-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="2eb36-134">Części ścieżki powinny być oddzielone kropką (.).</span><span class="sxs-lookup"><span data-stu-id="2eb36-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb36-135">-User</span><span class="sxs-lookup"><span data-stu-id="2eb36-135">-User</span></span>
<span data-ttu-id="2eb36-136">Usuwanie wpisu ACL wykazu dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2eb36-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb36-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2eb36-137">-Confirm</span></span>
<span data-ttu-id="2eb36-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb36-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb36-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb36-139">-WhatIf</span></span>
<span data-ttu-id="2eb36-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eb36-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb36-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2eb36-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb36-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb36-142">CommonParameters</span></span>
<span data-ttu-id="2eb36-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb36-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb36-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb36-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb36-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eb36-145">INPUTS</span></span>

### <span data-ttu-id="2eb36-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb36-146">System.String</span></span>

### <span data-ttu-id="2eb36-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2eb36-147">System.Guid</span></span>

### <span data-ttu-id="2eb36-148">Microsoft. Azure. Commands. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="2eb36-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="2eb36-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eb36-149">OUTPUTS</span></span>

### <span data-ttu-id="2eb36-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2eb36-150">System.Boolean</span></span>

## <span data-ttu-id="2eb36-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eb36-151">NOTES</span></span>

## <span data-ttu-id="2eb36-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eb36-152">RELATED LINKS</span></span>

[<span data-ttu-id="2eb36-153">Pozycja U — SQL oferuje teraz kontrolę dostępu na poziomie bazy danych</span><span class="sxs-lookup"><span data-stu-id="2eb36-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="2eb36-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2eb36-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="2eb36-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2eb36-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
