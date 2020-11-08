---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/22/2020
ms.locfileid: "94224099"
---
# <span data-ttu-id="9255b-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="9255b-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="9255b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9255b-102">SYNOPSIS</span></span>
<span data-ttu-id="9255b-103">Pobiera produkt z usługi Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9255b-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="9255b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9255b-104">SYNTAX</span></span>

### <span data-ttu-id="9255b-105">Products_Download (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9255b-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9255b-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="9255b-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9255b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9255b-107">DESCRIPTION</span></span>
<span data-ttu-id="9255b-108">Pobiera produkt z usługi Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9255b-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="9255b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9255b-109">EXAMPLES</span></span>

### <span data-ttu-id="9255b-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="9255b-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="9255b-111">Pobierz produkt z usługi Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="9255b-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="9255b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9255b-112">PARAMETERS</span></span>

### <span data-ttu-id="9255b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9255b-113">-Name</span></span>
<span data-ttu-id="9255b-114">Nazwa produktu</span><span class="sxs-lookup"><span data-stu-id="9255b-114">Name of the product</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9255b-115">-Activationname</span><span class="sxs-lookup"><span data-stu-id="9255b-115">-ActivationName</span></span>
<span data-ttu-id="9255b-116">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="9255b-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9255b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9255b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9255b-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="9255b-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9255b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9255b-119">-ResourceId</span></span>
<span data-ttu-id="9255b-120">Identyfikator zasobu dla produktu Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="9255b-120">Resource identifier for azure bridge product.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9255b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9255b-121">-AsJob</span></span>
<span data-ttu-id="9255b-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="9255b-122">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="9255b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9255b-123">-Force</span></span>
<span data-ttu-id="9255b-124">Parametr przełącznika nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="9255b-124">Switch parameter not to ask for confirmation</span></span>

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

### <span data-ttu-id="9255b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9255b-125">-WhatIf</span></span>
<span data-ttu-id="9255b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9255b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9255b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9255b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9255b-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9255b-128">-Confirm</span></span>
<span data-ttu-id="9255b-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9255b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9255b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9255b-130">CommonParameters</span></span>
<span data-ttu-id="9255b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9255b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9255b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9255b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9255b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9255b-133">INPUTS</span></span>

## <span data-ttu-id="9255b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9255b-134">OUTPUTS</span></span>

## <span data-ttu-id="9255b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9255b-135">NOTES</span></span>

## <span data-ttu-id="9255b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9255b-136">RELATED LINKS</span></span>
