---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: b5e9828c0cf9f73f88a44b7a4471a22bbfbe49af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544507"
---
# <span data-ttu-id="2ce3f-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2ce3f-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="2ce3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ce3f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce3f-103">Tworzy zestaw dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ce3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ce3f-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [<CommonParameters>]
```

## <span data-ttu-id="2ce3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ce3f-105">DESCRIPTION</span></span>
<span data-ttu-id="2ce3f-106">Polecenie cmdlet **New-AzureRmAvailabilitySet** umożliwia utworzenie zestawu dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="2ce3f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ce3f-107">EXAMPLES</span></span>

### <span data-ttu-id="2ce3f-108">Przykład 1. Tworzenie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="2ce3f-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="2ce3f-109">To polecenie tworzy zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2ce3f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ce3f-110">PARAMETERS</span></span>

### <span data-ttu-id="2ce3f-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2ce3f-111">-Location</span></span>
<span data-ttu-id="2ce3f-112">Określa lokalizację zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-112">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce3f-113">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="2ce3f-113">-Managed</span></span>
<span data-ttu-id="2ce3f-114">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="2ce3f-114">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce3f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ce3f-115">-Name</span></span>
<span data-ttu-id="2ce3f-116">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-116">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce3f-117">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="2ce3f-117">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="2ce3f-118">Określa liczbę domen błędów platformy.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-118">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce3f-119">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="2ce3f-119">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="2ce3f-120">Określa liczbę domen aktualizacji platformy.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-120">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce3f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ce3f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ce3f-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce3f-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ce3f-123">-Sku</span></span>
<span data-ttu-id="2ce3f-124">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="2ce3f-124">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce3f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce3f-125">CommonParameters</span></span>
<span data-ttu-id="2ce3f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce3f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ce3f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce3f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ce3f-128">INPUTS</span></span>

### <span data-ttu-id="2ce3f-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2ce3f-129">None</span></span>
<span data-ttu-id="2ce3f-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2ce3f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ce3f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ce3f-131">OUTPUTS</span></span>

## <span data-ttu-id="2ce3f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ce3f-132">NOTES</span></span>

## <span data-ttu-id="2ce3f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ce3f-133">RELATED LINKS</span></span>

[<span data-ttu-id="2ce3f-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2ce3f-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="2ce3f-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2ce3f-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


