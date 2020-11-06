---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554208"
---
# <span data-ttu-id="1b419-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1b419-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="1b419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b419-102">SYNOPSIS</span></span>
<span data-ttu-id="1b419-103">Tworzy zestaw dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1b419-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b419-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b419-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b419-105">DESCRIPTION</span></span>
<span data-ttu-id="1b419-106">Polecenie cmdlet **New-AzureRmAvailabilitySet** umożliwia utworzenie zestawu dostępności na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1b419-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="1b419-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b419-107">EXAMPLES</span></span>

### <span data-ttu-id="1b419-108">Przykład 1. Tworzenie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="1b419-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="1b419-109">To polecenie tworzy zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1b419-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1b419-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b419-110">PARAMETERS</span></span>

### <span data-ttu-id="1b419-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b419-111">-DefaultProfile</span></span>
<span data-ttu-id="1b419-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b419-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b419-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1b419-113">-Location</span></span>
<span data-ttu-id="1b419-114">Określa lokalizację zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="1b419-114">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="1b419-115">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="1b419-115">-Managed</span></span>
<span data-ttu-id="1b419-116">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="1b419-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b419-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b419-117">-Name</span></span>
<span data-ttu-id="1b419-118">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="1b419-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="1b419-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="1b419-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="1b419-120">Określa liczbę domen błędów platformy.</span><span class="sxs-lookup"><span data-stu-id="1b419-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="1b419-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="1b419-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="1b419-122">Określa liczbę domen aktualizacji platformy.</span><span class="sxs-lookup"><span data-stu-id="1b419-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="1b419-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b419-123">-ResourceGroupName</span></span>
<span data-ttu-id="1b419-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b419-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1b419-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="1b419-125">-Sku</span></span>
<span data-ttu-id="1b419-126">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="1b419-126">The Name of Sku</span></span>
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

### <span data-ttu-id="1b419-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b419-127">CommonParameters</span></span>
<span data-ttu-id="1b419-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b419-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b419-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b419-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b419-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b419-130">INPUTS</span></span>

## <span data-ttu-id="1b419-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b419-131">OUTPUTS</span></span>

## <span data-ttu-id="1b419-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b419-132">NOTES</span></span>

## <span data-ttu-id="1b419-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b419-133">RELATED LINKS</span></span>

[<span data-ttu-id="1b419-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1b419-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="1b419-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1b419-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


