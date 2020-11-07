---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bde5ca1c9a354e78f04ec3c9a54da72617f7ecc5
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/22/2020
ms.locfileid: "93719704"
---
# <span data-ttu-id="46880-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="46880-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="46880-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46880-102">SYNOPSIS</span></span>
<span data-ttu-id="46880-103">Usuwanie produktu pobranego z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="46880-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="46880-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46880-104">SYNTAX</span></span>

### <span data-ttu-id="46880-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="46880-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46880-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="46880-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46880-107">Opis</span><span class="sxs-lookup"><span data-stu-id="46880-107">DESCRIPTION</span></span>
<span data-ttu-id="46880-108">Usuwanie produktu pobranego z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="46880-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="46880-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46880-109">EXAMPLES</span></span>

### <span data-ttu-id="46880-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46880-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="46880-111">Usuwanie produktu pobranego z usługi Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="46880-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="46880-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46880-112">PARAMETERS</span></span>

### <span data-ttu-id="46880-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="46880-113">-ActivationName</span></span>
<span data-ttu-id="46880-114">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="46880-114">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46880-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46880-115">-AsJob</span></span>
<span data-ttu-id="46880-116">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="46880-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="46880-117">-Force</span><span class="sxs-lookup"><span data-stu-id="46880-117">-Force</span></span>
<span data-ttu-id="46880-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46880-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="46880-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46880-119">-Name</span></span>
<span data-ttu-id="46880-120">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="46880-120">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46880-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46880-121">-ResourceGroupName</span></span>
<span data-ttu-id="46880-122">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="46880-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46880-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46880-123">-ResourceId</span></span>
<span data-ttu-id="46880-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="46880-124">The resource id.</span></span>

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

### <span data-ttu-id="46880-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46880-125">-Confirm</span></span>
<span data-ttu-id="46880-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46880-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46880-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46880-127">-WhatIf</span></span>
<span data-ttu-id="46880-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46880-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46880-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46880-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46880-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46880-130">CommonParameters</span></span>
<span data-ttu-id="46880-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46880-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46880-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46880-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46880-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46880-133">INPUTS</span></span>

## <span data-ttu-id="46880-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46880-134">OUTPUTS</span></span>

### <span data-ttu-id="46880-135">Microsoft. AzureStack. Management. AzureBridge. admin. models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="46880-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="46880-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46880-136">NOTES</span></span>

## <span data-ttu-id="46880-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46880-137">RELATED LINKS</span></span>

