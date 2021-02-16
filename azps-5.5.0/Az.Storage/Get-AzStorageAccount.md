---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187819"
---
# <span data-ttu-id="225fa-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="225fa-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="225fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="225fa-102">SYNOPSIS</span></span>
<span data-ttu-id="225fa-103">Otrzymuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="225fa-103">Gets a Storage account.</span></span>

## <span data-ttu-id="225fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="225fa-104">SYNTAX</span></span>

### <span data-ttu-id="225fa-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="225fa-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="225fa-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="225fa-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="225fa-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="225fa-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="225fa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="225fa-108">DESCRIPTION</span></span>
<span data-ttu-id="225fa-109">Polecenie **cmdlet Get-AzStorageAccount** otrzymuje określone konto magazynu lub wszystkie konta magazynu w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="225fa-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="225fa-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="225fa-110">EXAMPLES</span></span>

### <span data-ttu-id="225fa-111">Przykład 1. Uzyskiwanie określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="225fa-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="225fa-112">To polecenie otrzymuje określone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="225fa-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="225fa-113">Przykład 2. Uzyskiwanie wszystkich kont magazynu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="225fa-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="225fa-114">To polecenie pobiera wszystkie konta magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="225fa-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="225fa-115">Przykład 3. Uzyskiwanie wszystkich kont magazynu w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="225fa-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="225fa-116">To polecenie pobiera wszystkie konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="225fa-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="225fa-117">Przykład 4. Uzyskiwanie kont magazynu ze stanem przywracania obiektów blob</span><span class="sxs-lookup"><span data-stu-id="225fa-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="225fa-118">To polecenie otrzymuje konta magazynu ze stanem przywracania obiektów blob i wyświetla stan przywracania obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="225fa-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="225fa-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="225fa-119">PARAMETERS</span></span>

### <span data-ttu-id="225fa-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="225fa-120">-AsJob</span></span>
<span data-ttu-id="225fa-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="225fa-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="225fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225fa-122">-DefaultProfile</span></span>
<span data-ttu-id="225fa-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="225fa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="225fa-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="225fa-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="225fa-125">Pobierz obiekt BlobRestoreStatus konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="225fa-125">Get the BlobRestoreStatus of the Storage account.</span></span>

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

### <span data-ttu-id="225fa-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="225fa-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="225fa-127">Pobierz dane GeoReplicationStats konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="225fa-127">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="225fa-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="225fa-128">-Name</span></span>
<span data-ttu-id="225fa-129">Określa nazwę konta magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="225fa-129">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="225fa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225fa-130">-ResourceGroupName</span></span>
<span data-ttu-id="225fa-131">Określa nazwę grupy zasobów zawierającej konto magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="225fa-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="225fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225fa-132">CommonParameters</span></span>
<span data-ttu-id="225fa-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225fa-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225fa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225fa-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="225fa-135">INPUTS</span></span>

### <span data-ttu-id="225fa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="225fa-136">System.String</span></span>

## <span data-ttu-id="225fa-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="225fa-137">OUTPUTS</span></span>

### <span data-ttu-id="225fa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="225fa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="225fa-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="225fa-139">NOTES</span></span>

## <span data-ttu-id="225fa-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="225fa-140">RELATED LINKS</span></span>

[<span data-ttu-id="225fa-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="225fa-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="225fa-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="225fa-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="225fa-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="225fa-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


