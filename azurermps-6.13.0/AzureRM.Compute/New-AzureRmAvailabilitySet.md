---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718627"
---
# <span data-ttu-id="92496-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92496-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="92496-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92496-102">SYNOPSIS</span></span>
<span data-ttu-id="92496-103">Tworzy zestaw dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="92496-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92496-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92496-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92496-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92496-105">DESCRIPTION</span></span>
<span data-ttu-id="92496-106">Polecenie cmdlet **New-AzureRmAvailabilitySet** umożliwia utworzenie zestawu dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="92496-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="92496-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92496-107">EXAMPLES</span></span>

### <span data-ttu-id="92496-108">Przykład 1. Tworzenie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="92496-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="92496-109">To polecenie tworzy zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="92496-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="92496-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92496-110">PARAMETERS</span></span>

### <span data-ttu-id="92496-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92496-111">-AsJob</span></span>
<span data-ttu-id="92496-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="92496-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="92496-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92496-113">-DefaultProfile</span></span>
<span data-ttu-id="92496-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92496-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92496-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="92496-115">-Location</span></span>
<span data-ttu-id="92496-116">Określa lokalizację zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="92496-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="92496-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92496-117">-Name</span></span>
<span data-ttu-id="92496-118">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="92496-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92496-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="92496-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="92496-120">Określa liczbę domen błędów platformy.</span><span class="sxs-lookup"><span data-stu-id="92496-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92496-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="92496-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="92496-122">Określa liczbę domen aktualizacji platformy.</span><span class="sxs-lookup"><span data-stu-id="92496-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92496-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92496-123">-ResourceGroupName</span></span>
<span data-ttu-id="92496-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92496-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92496-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="92496-125">-Sku</span></span>
<span data-ttu-id="92496-126">Nazwa SKU.</span><span class="sxs-lookup"><span data-stu-id="92496-126">The Name of Sku.</span></span>
<span data-ttu-id="92496-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="92496-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92496-128">Wyrównanie: dla dysków zarządzanych</span><span class="sxs-lookup"><span data-stu-id="92496-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="92496-129">Klasyczny: dla dysków niezarządzanych</span><span class="sxs-lookup"><span data-stu-id="92496-129">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92496-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="92496-130">-Tag</span></span>
<span data-ttu-id="92496-131">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="92496-131">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92496-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92496-132">CommonParameters</span></span>
<span data-ttu-id="92496-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92496-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92496-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92496-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92496-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92496-135">INPUTS</span></span>

### <span data-ttu-id="92496-136">System. String</span><span class="sxs-lookup"><span data-stu-id="92496-136">System.String</span></span>

### <span data-ttu-id="92496-137">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="92496-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="92496-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92496-138">OUTPUTS</span></span>

### <span data-ttu-id="92496-139">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92496-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="92496-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92496-140">NOTES</span></span>

## <span data-ttu-id="92496-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92496-141">RELATED LINKS</span></span>

[<span data-ttu-id="92496-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92496-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="92496-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92496-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


