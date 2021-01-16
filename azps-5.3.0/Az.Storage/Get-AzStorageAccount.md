---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376271"
---
# <span data-ttu-id="d952b-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d952b-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="d952b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d952b-102">SYNOPSIS</span></span>
<span data-ttu-id="d952b-103">Pobiera konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d952b-103">Gets a Storage account.</span></span>

## <span data-ttu-id="d952b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d952b-104">SYNTAX</span></span>

### <span data-ttu-id="d952b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d952b-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d952b-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d952b-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d952b-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="d952b-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d952b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d952b-108">DESCRIPTION</span></span>
<span data-ttu-id="d952b-109">Polecenie cmdlet **Get-AzStorageAccount** pobiera określone konto magazynu lub wszystkie konta magazynu w grupie zasobów lub abonament.</span><span class="sxs-lookup"><span data-stu-id="d952b-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="d952b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d952b-110">EXAMPLES</span></span>

### <span data-ttu-id="d952b-111">Przykład 1: uzyskiwanie określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d952b-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="d952b-112">To polecenie pobiera określone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d952b-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="d952b-113">Przykład 2: pobieranie wszystkich kont magazynu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d952b-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="d952b-114">To polecenie umożliwia pobieranie wszystkich kont magazynu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d952b-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="d952b-115">Przykład 3: uzyskiwanie wszystkich kont magazynu w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d952b-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="d952b-116">To polecenie umożliwia pobieranie wszystkich kont magazynu w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d952b-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="d952b-117">Przykład 4: uzyskiwanie kont magazynu przy użyciu stanu przywracania obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="d952b-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="d952b-118">To polecenie umożliwia pobieranie kont magazynu wraz z ich stanem przywracania i wyświetlanie stanu przywracania obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="d952b-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="d952b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d952b-119">PARAMETERS</span></span>

### <span data-ttu-id="d952b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d952b-120">-AsJob</span></span>
<span data-ttu-id="d952b-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d952b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d952b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d952b-122">-DefaultProfile</span></span>
<span data-ttu-id="d952b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d952b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d952b-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="d952b-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="d952b-125">Pobierz BlobRestoreStatus konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d952b-125">Get the BlobRestoreStatus of the Storage account.</span></span>

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

### <span data-ttu-id="d952b-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="d952b-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="d952b-127">Pobierz GeoReplicationStats konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d952b-127">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="d952b-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d952b-128">-Name</span></span>
<span data-ttu-id="d952b-129">Określa nazwę konta magazynu, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="d952b-129">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="d952b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d952b-130">-ResourceGroupName</span></span>
<span data-ttu-id="d952b-131">Określa nazwę grupy zasobów zawierającej konto magazynu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d952b-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="d952b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d952b-132">CommonParameters</span></span>
<span data-ttu-id="d952b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d952b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d952b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d952b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d952b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d952b-135">INPUTS</span></span>

### <span data-ttu-id="d952b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d952b-136">System.String</span></span>

## <span data-ttu-id="d952b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d952b-137">OUTPUTS</span></span>

### <span data-ttu-id="d952b-138">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d952b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d952b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d952b-139">NOTES</span></span>

## <span data-ttu-id="d952b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d952b-140">RELATED LINKS</span></span>

[<span data-ttu-id="d952b-141">Nowe — AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d952b-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="d952b-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d952b-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="d952b-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d952b-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


