---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9374f8a55beca561afd9ed4bca4320b685349798
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/22/2020
ms.locfileid: "93899450"
---
# <span data-ttu-id="38efe-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="38efe-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="38efe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38efe-102">SYNOPSIS</span></span>
<span data-ttu-id="38efe-103">Zwraca aktywację mostka Azure.</span><span class="sxs-lookup"><span data-stu-id="38efe-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="38efe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38efe-104">SYNTAX</span></span>

### <span data-ttu-id="38efe-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="38efe-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="38efe-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="38efe-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="38efe-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="38efe-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="38efe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="38efe-108">DESCRIPTION</span></span>
<span data-ttu-id="38efe-109">Po zarejestrowaniu stosu platformy Azure obiekt aktywacji zawiera informacje, które łączą wdrożenie stosu platformy Azure do swojej rejestracji na platformie Azure, na przykład datę wygaśnięcia rejestracji, nazwę itd.</span><span class="sxs-lookup"><span data-stu-id="38efe-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="38efe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38efe-110">EXAMPLES</span></span>

### <span data-ttu-id="38efe-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="38efe-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="38efe-112">Uzyskiwanie listy aktywacji usługi Azure Bridge w grupie zasobów "activationRG"</span><span class="sxs-lookup"><span data-stu-id="38efe-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="38efe-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="38efe-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="38efe-114">Uzyskiwanie aktywacji usługi Azure Bridge na podstawie nazwy "Moja Aktywacja" znajdującej się w obszarze "activationRG"</span><span class="sxs-lookup"><span data-stu-id="38efe-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="38efe-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38efe-115">PARAMETERS</span></span>

### <span data-ttu-id="38efe-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38efe-116">-Name</span></span>
<span data-ttu-id="38efe-117">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="38efe-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38efe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38efe-118">-ResourceGroupName</span></span>
<span data-ttu-id="38efe-119">Grupa zasobów używana podczas rejestracji stosu platformy Azure; Możesz również wyświetlić nazwy grup zasobów w portalu.</span><span class="sxs-lookup"><span data-stu-id="38efe-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38efe-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38efe-120">-ResourceId</span></span>
<span data-ttu-id="38efe-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="38efe-121">The resource id.</span></span>

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

### <span data-ttu-id="38efe-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="38efe-122">-Skip</span></span>
<span data-ttu-id="38efe-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="38efe-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38efe-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="38efe-124">-Top</span></span>
<span data-ttu-id="38efe-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="38efe-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="38efe-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="38efe-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38efe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38efe-127">CommonParameters</span></span>
<span data-ttu-id="38efe-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38efe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38efe-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38efe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38efe-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38efe-130">INPUTS</span></span>

## <span data-ttu-id="38efe-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38efe-131">OUTPUTS</span></span>

### <span data-ttu-id="38efe-132">Microsoft. AzureStack. Management. AzureBridge. admin. models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="38efe-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="38efe-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38efe-133">NOTES</span></span>

## <span data-ttu-id="38efe-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38efe-134">RELATED LINKS</span></span>
