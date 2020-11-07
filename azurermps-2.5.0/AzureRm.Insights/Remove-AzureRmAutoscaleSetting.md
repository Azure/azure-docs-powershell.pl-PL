---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898450"
---
# <span data-ttu-id="65e3f-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="65e3f-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="65e3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="65e3f-103">Usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="65e3f-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65e3f-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65e3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65e3f-105">DESCRIPTION</span></span>
<span data-ttu-id="65e3f-106">Polecenie cmdlet **Remove-AzureRmAutoscaleSetting** usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="65e3f-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="65e3f-107">Musisz określić nazwę ustawienia oraz nazwę grupy zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="65e3f-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="65e3f-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="65e3f-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="65e3f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65e3f-109">EXAMPLES</span></span>

## <span data-ttu-id="65e3f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65e3f-110">PARAMETERS</span></span>

### <span data-ttu-id="65e3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e3f-111">-DefaultProfile</span></span>
<span data-ttu-id="65e3f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="65e3f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65e3f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65e3f-113">-Name</span></span>
<span data-ttu-id="65e3f-114">Określa nazwę ustawienia skalowania automatycznego, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="65e3f-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e3f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e3f-115">-ResourceGroupName</span></span>
<span data-ttu-id="65e3f-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65e3f-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e3f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65e3f-117">-Confirm</span></span>
<span data-ttu-id="65e3f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e3f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e3f-119">-WhatIf</span></span>
<span data-ttu-id="65e3f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e3f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65e3f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65e3f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e3f-122">CommonParameters</span></span>
<span data-ttu-id="65e3f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e3f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e3f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e3f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65e3f-125">INPUTS</span></span>

### <span data-ttu-id="65e3f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="65e3f-126">System.String</span></span>

## <span data-ttu-id="65e3f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65e3f-127">OUTPUTS</span></span>

### <span data-ttu-id="65e3f-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="65e3f-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="65e3f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65e3f-129">NOTES</span></span>

## <span data-ttu-id="65e3f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65e3f-130">RELATED LINKS</span></span>

[<span data-ttu-id="65e3f-131">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="65e3f-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="65e3f-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="65e3f-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


