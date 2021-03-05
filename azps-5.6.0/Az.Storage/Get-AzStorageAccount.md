---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: 2c8980f198dc675e12a9b9c6048a4960c1998f9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002810"
---
# <span data-ttu-id="c2e82-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2e82-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="c2e82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2e82-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e82-103">Otrzymuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2e82-103">Gets a Storage account.</span></span>

## <span data-ttu-id="c2e82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2e82-104">SYNTAX</span></span>

### <span data-ttu-id="c2e82-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e82-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2e82-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e82-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2e82-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e82-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2e82-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2e82-108">DESCRIPTION</span></span>
<span data-ttu-id="c2e82-109">Polecenie **cmdlet Get-AzStorageAccount** pobiera określone konto magazynu lub wszystkie konta magazynu w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c2e82-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="c2e82-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2e82-110">EXAMPLES</span></span>

### <span data-ttu-id="c2e82-111">Przykład 1. Uzyskiwanie określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="c2e82-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="c2e82-112">To polecenie otrzymuje określone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2e82-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="c2e82-113">Przykład 2. Uzyskiwanie wszystkich kont magazynu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c2e82-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="c2e82-114">To polecenie pobiera wszystkie konta magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2e82-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="c2e82-115">Przykład 3. Uzyskiwanie wszystkich kont magazynu w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c2e82-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="c2e82-116">To polecenie pobiera wszystkie konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c2e82-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="c2e82-117">Przykład 4. Uzyskiwanie kont magazynu ze stanem przywracania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="c2e82-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="c2e82-118">To polecenie otrzymuje konta magazynu ze stanem przywracania obiektów blob i wyświetla stan przywracania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="c2e82-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="c2e82-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2e82-119">PARAMETERS</span></span>

### <span data-ttu-id="c2e82-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c2e82-120">-AsJob</span></span>
<span data-ttu-id="c2e82-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c2e82-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2e82-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e82-122">-DefaultProfile</span></span>
<span data-ttu-id="c2e82-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e82-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2e82-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="c2e82-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="c2e82-125">Pobierz obiekt BlobRestoreStatus konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2e82-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e82-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="c2e82-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="c2e82-127">Pobierz dane GeoReplicationStats konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2e82-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e82-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2e82-128">-Name</span></span>
<span data-ttu-id="c2e82-129">Określa nazwę konta magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="c2e82-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e82-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2e82-130">-ResourceGroupName</span></span>
<span data-ttu-id="c2e82-131">Określa nazwę grupy zasobów zawierającej konto magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="c2e82-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e82-132">CommonParameters</span></span>
<span data-ttu-id="c2e82-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e82-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2e82-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e82-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2e82-135">INPUTS</span></span>

### <span data-ttu-id="c2e82-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c2e82-136">System.String</span></span>

## <span data-ttu-id="c2e82-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2e82-137">OUTPUTS</span></span>

### <span data-ttu-id="c2e82-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2e82-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c2e82-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2e82-139">NOTES</span></span>

## <span data-ttu-id="c2e82-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2e82-140">RELATED LINKS</span></span>

[<span data-ttu-id="c2e82-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2e82-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="c2e82-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2e82-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="c2e82-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2e82-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


