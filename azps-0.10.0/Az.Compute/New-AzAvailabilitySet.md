---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893670"
---
# <span data-ttu-id="37656-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="37656-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="37656-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37656-102">SYNOPSIS</span></span>
<span data-ttu-id="37656-103">Tworzy zestaw dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="37656-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="37656-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37656-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37656-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37656-105">DESCRIPTION</span></span>
<span data-ttu-id="37656-106">Polecenie cmdlet **New-AzAvailabilitySet** umożliwia utworzenie zestawu dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="37656-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="37656-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37656-107">EXAMPLES</span></span>

### <span data-ttu-id="37656-108">Przykład 1. Tworzenie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="37656-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="37656-109">To polecenie tworzy zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="37656-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="37656-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37656-110">PARAMETERS</span></span>

### <span data-ttu-id="37656-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37656-111">-AsJob</span></span>
<span data-ttu-id="37656-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="37656-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37656-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37656-113">-DefaultProfile</span></span>
<span data-ttu-id="37656-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37656-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37656-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="37656-115">-Location</span></span>
<span data-ttu-id="37656-116">Określa lokalizację zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="37656-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="37656-117">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="37656-117">-Managed</span></span>
<span data-ttu-id="37656-118">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="37656-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="37656-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37656-119">-Name</span></span>
<span data-ttu-id="37656-120">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="37656-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="37656-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="37656-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="37656-122">Określa liczbę domen błędów platformy.</span><span class="sxs-lookup"><span data-stu-id="37656-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="37656-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="37656-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="37656-124">Określa liczbę domen aktualizacji platformy.</span><span class="sxs-lookup"><span data-stu-id="37656-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="37656-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37656-125">-ResourceGroupName</span></span>
<span data-ttu-id="37656-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37656-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="37656-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="37656-127">-Sku</span></span>
<span data-ttu-id="37656-128">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="37656-128">The Name of Sku</span></span>
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

### <span data-ttu-id="37656-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37656-129">CommonParameters</span></span>
<span data-ttu-id="37656-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37656-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37656-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37656-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37656-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37656-132">INPUTS</span></span>

### <span data-ttu-id="37656-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="37656-133">None</span></span>
<span data-ttu-id="37656-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="37656-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37656-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37656-135">OUTPUTS</span></span>

### <span data-ttu-id="37656-136">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="37656-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="37656-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37656-137">NOTES</span></span>

## <span data-ttu-id="37656-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37656-138">RELATED LINKS</span></span>

[<span data-ttu-id="37656-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="37656-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="37656-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="37656-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


