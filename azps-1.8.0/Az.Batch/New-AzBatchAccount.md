---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: e996e02c9609e259c0833cfe179f295206684351
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710830"
---
# <span data-ttu-id="170c4-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="170c4-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="170c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="170c4-102">SYNOPSIS</span></span>
<span data-ttu-id="170c4-103">Tworzy konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="170c4-103">Creates a Batch account.</span></span>

## <span data-ttu-id="170c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="170c4-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="170c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="170c4-105">DESCRIPTION</span></span>
<span data-ttu-id="170c4-106">Polecenie cmdlet **New-AzBatchAccount** tworzy konto usługi Azure Batch dla określonej grupy zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="170c4-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="170c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="170c4-107">EXAMPLES</span></span>

### <span data-ttu-id="170c4-108">Przykład 1. Tworzenie konta wsadowego</span><span class="sxs-lookup"><span data-stu-id="170c4-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="170c4-109">To polecenie tworzy konto wsadowe o nazwie pfuller przy użyciu ResourceGroup03 grupy zasobów w zachodniej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="170c4-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="170c4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="170c4-110">PARAMETERS</span></span>

### <span data-ttu-id="170c4-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="170c4-111">-AccountName</span></span>
<span data-ttu-id="170c4-112">Określa nazwę konta wsadowego tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="170c4-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="170c4-113">Nazwy kont wsadowych muszą mieć od 3 do 24 znaków i zawierać tylko cyfry i małe litery.</span><span class="sxs-lookup"><span data-stu-id="170c4-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="170c4-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="170c4-115">Określa identyfikator zasobu konta magazynu, który ma być wykorzystywany do automatycznego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="170c4-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170c4-116">-DefaultProfile</span></span>
<span data-ttu-id="170c4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="170c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170c4-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="170c4-118">-KeyVaultId</span></span>
<span data-ttu-id="170c4-119">Identyfikator zasobu magazynu kluczy platformy Azure skojarzonego z kontem wsadowym.</span><span class="sxs-lookup"><span data-stu-id="170c4-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="170c4-120">-KeyVaultUrl</span></span>
<span data-ttu-id="170c4-121">Adres URL magazynu kluczy platformy Azure skojarzonego z kontem wsadowym.</span><span class="sxs-lookup"><span data-stu-id="170c4-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="170c4-122">-Location</span></span>
<span data-ttu-id="170c4-123">Określa region, w którym to polecenie cmdlet tworzy konto.</span><span class="sxs-lookup"><span data-stu-id="170c4-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="170c4-124">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="170c4-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="170c4-125">-PoolAllocationMode</span></span>
<span data-ttu-id="170c4-126">Tryb przydziału służący do tworzenia pul na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="170c4-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="170c4-128">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy konto.</span><span class="sxs-lookup"><span data-stu-id="170c4-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="170c4-129">-Tag</span></span>
<span data-ttu-id="170c4-130">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="170c4-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="170c4-131">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="170c4-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170c4-132">CommonParameters</span></span>
<span data-ttu-id="170c4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170c4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170c4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170c4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="170c4-135">INPUTS</span></span>

### <span data-ttu-id="170c4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="170c4-136">System.String</span></span>

### <span data-ttu-id="170c4-137">System. Nullable "1 [[Microsoft.Azure.Management.Batch. Modele. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="170c4-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="170c4-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="170c4-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="170c4-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="170c4-139">OUTPUTS</span></span>

### <span data-ttu-id="170c4-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="170c4-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="170c4-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="170c4-141">NOTES</span></span>

## <span data-ttu-id="170c4-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="170c4-142">RELATED LINKS</span></span>

[<span data-ttu-id="170c4-143">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="170c4-143">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="170c4-144">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="170c4-144">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="170c4-145">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="170c4-145">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="170c4-146">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="170c4-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
