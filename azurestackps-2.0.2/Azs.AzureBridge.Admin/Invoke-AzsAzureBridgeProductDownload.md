---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7ca58f806f4d63f2938e3934838a40cbbb113b2
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/26/2020
ms.locfileid: "94061802"
---
# <span data-ttu-id="698f2-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="698f2-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="698f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="698f2-102">SYNOPSIS</span></span>
<span data-ttu-id="698f2-103">Pobiera produkt z usługi Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="698f2-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="698f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="698f2-104">SYNTAX</span></span>

### <span data-ttu-id="698f2-105">Products_Download (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="698f2-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="698f2-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="698f2-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="698f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="698f2-107">DESCRIPTION</span></span>
<span data-ttu-id="698f2-108">Pobiera produkt z usługi Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="698f2-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="698f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="698f2-109">EXAMPLES</span></span>

### <span data-ttu-id="698f2-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="698f2-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="698f2-111">Pobierz produkt z usługi Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="698f2-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="698f2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="698f2-112">PARAMETERS</span></span>

### <span data-ttu-id="698f2-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="698f2-113">-ActivationName</span></span>
<span data-ttu-id="698f2-114">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="698f2-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="698f2-115">-AsJob</span></span>
<span data-ttu-id="698f2-116">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="698f2-116">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="698f2-117">-Force</span></span>
<span data-ttu-id="698f2-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="698f2-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="698f2-119">-Name</span></span>
<span data-ttu-id="698f2-120">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="698f2-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="698f2-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="698f2-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="698f2-123">-ResourceId</span></span>
<span data-ttu-id="698f2-124">Identyfikator zasobu dla produktu Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="698f2-124">Resource identifier for azure bridge product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="698f2-125">-Confirm</span></span>
<span data-ttu-id="698f2-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="698f2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="698f2-127">-WhatIf</span></span>
<span data-ttu-id="698f2-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="698f2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="698f2-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="698f2-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698f2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698f2-130">CommonParameters</span></span>
<span data-ttu-id="698f2-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698f2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698f2-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698f2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698f2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="698f2-133">INPUTS</span></span>

## <span data-ttu-id="698f2-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="698f2-134">OUTPUTS</span></span>

## <span data-ttu-id="698f2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="698f2-135">NOTES</span></span>

## <span data-ttu-id="698f2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="698f2-136">RELATED LINKS</span></span>

