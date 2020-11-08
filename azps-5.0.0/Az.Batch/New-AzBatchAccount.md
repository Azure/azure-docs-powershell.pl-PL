---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: db35d5f6f0a8c8345fb10d13e4d2ca5c6169a090
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232128"
---
# <span data-ttu-id="0fbb5-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0fbb5-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="0fbb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbb5-103">Tworzy konto wsadowe.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-103">Creates a Batch account.</span></span>

## <span data-ttu-id="0fbb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fbb5-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbb5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0fbb5-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbb5-106">Polecenie cmdlet **New-AzBatchAccount** tworzy konto usługi Azure Batch dla określonej grupy zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="0fbb5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fbb5-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbb5-108">Przykład 1. Tworzenie konta wsadowego</span><span class="sxs-lookup"><span data-stu-id="0fbb5-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="0fbb5-109">To polecenie tworzy konto wsadowe o nazwie pfuller przy użyciu ResourceGroup03 grupy zasobów w zachodniej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="0fbb5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fbb5-110">PARAMETERS</span></span>

### <span data-ttu-id="0fbb5-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0fbb5-111">-AccountName</span></span>
<span data-ttu-id="0fbb5-112">Określa nazwę konta wsadowego tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="0fbb5-113">Nazwy kont wsadowych muszą mieć od 3 do 24 znaków i zawierać tylko cyfry i małe litery.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="0fbb5-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0fbb5-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="0fbb5-115">Określa identyfikator zasobu konta magazynu, który ma być wykorzystywany do automatycznego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="0fbb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbb5-116">-DefaultProfile</span></span>
<span data-ttu-id="0fbb5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbb5-118">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0fbb5-118">-IdentityType</span></span>
<span data-ttu-id="0fbb5-119">Tożsamość skojarzona z BatchAccount</span><span class="sxs-lookup"><span data-stu-id="0fbb5-119">The identity associated with the BatchAccount</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fbb5-120">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0fbb5-120">-KeyVaultId</span></span>
<span data-ttu-id="0fbb5-121">Identyfikator zasobu magazynu kluczy platformy Azure skojarzonego z kontem wsadowym.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-121">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="0fbb5-122">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0fbb5-122">-KeyVaultUrl</span></span>
<span data-ttu-id="0fbb5-123">Adres URL magazynu kluczy platformy Azure skojarzonego z kontem wsadowym.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-123">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="0fbb5-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0fbb5-124">-Location</span></span>
<span data-ttu-id="0fbb5-125">Określa region, w którym to polecenie cmdlet tworzy konto.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-125">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="0fbb5-126">Aby uzyskać więcej informacji, zobacz [regiony platformy Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="0fbb5-126">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="0fbb5-127">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="0fbb5-127">-PoolAllocationMode</span></span>
<span data-ttu-id="0fbb5-128">Tryb przydziału służący do tworzenia pul na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-128">The allocation mode for creating pools in the Batch account.</span></span>

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

### <span data-ttu-id="0fbb5-129">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0fbb5-129">-PublicNetworkAccess</span></span>
<span data-ttu-id="0fbb5-130">Typ dostępu do sieci publicznej</span><span class="sxs-lookup"><span data-stu-id="0fbb5-130">The public network access type</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fbb5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbb5-131">-ResourceGroupName</span></span>
<span data-ttu-id="0fbb5-132">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy konto.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-132">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="0fbb5-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fbb5-133">-Tag</span></span>
<span data-ttu-id="0fbb5-134">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0fbb5-135">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0fbb5-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0fbb5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbb5-136">CommonParameters</span></span>
<span data-ttu-id="0fbb5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbb5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbb5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fbb5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbb5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fbb5-139">INPUTS</span></span>

### <span data-ttu-id="0fbb5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0fbb5-140">System.String</span></span>

### <span data-ttu-id="0fbb5-141">System. Nullable "1 [[Microsoft.Azure.Management.Batch. Modele. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 9.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0fbb5-141">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0fbb5-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0fbb5-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0fbb5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fbb5-143">OUTPUTS</span></span>

### <span data-ttu-id="0fbb5-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0fbb5-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0fbb5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fbb5-145">NOTES</span></span>

## <span data-ttu-id="0fbb5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fbb5-146">RELATED LINKS</span></span>

[<span data-ttu-id="0fbb5-147">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0fbb5-147">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="0fbb5-148">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0fbb5-148">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="0fbb5-149">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0fbb5-149">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="0fbb5-150">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0fbb5-150">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
