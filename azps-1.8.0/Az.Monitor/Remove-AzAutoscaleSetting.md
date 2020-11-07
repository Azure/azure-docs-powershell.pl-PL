---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: c5fcd5f4e331c55fb95a0d8657a59a944be585c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709764"
---
# <span data-ttu-id="adccb-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="adccb-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="adccb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="adccb-102">SYNOPSIS</span></span>
<span data-ttu-id="adccb-103">Usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="adccb-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="adccb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="adccb-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adccb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="adccb-105">DESCRIPTION</span></span>
<span data-ttu-id="adccb-106">Polecenie cmdlet **Remove-AzAutoscaleSetting** usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="adccb-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="adccb-107">Musisz określić nazwę ustawienia oraz nazwę grupy zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="adccb-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="adccb-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="adccb-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="adccb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="adccb-109">EXAMPLES</span></span>

## <span data-ttu-id="adccb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="adccb-110">PARAMETERS</span></span>

### <span data-ttu-id="adccb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adccb-111">-DefaultProfile</span></span>
<span data-ttu-id="adccb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="adccb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adccb-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="adccb-113">-Name</span></span>
<span data-ttu-id="adccb-114">Określa nazwę ustawienia skalowania automatycznego, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="adccb-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="adccb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adccb-115">-ResourceGroupName</span></span>
<span data-ttu-id="adccb-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="adccb-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="adccb-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adccb-117">-Confirm</span></span>
<span data-ttu-id="adccb-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adccb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adccb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adccb-119">-WhatIf</span></span>
<span data-ttu-id="adccb-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adccb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adccb-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="adccb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adccb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adccb-122">CommonParameters</span></span>
<span data-ttu-id="adccb-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adccb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adccb-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adccb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adccb-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adccb-125">INPUTS</span></span>

### <span data-ttu-id="adccb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="adccb-126">System.String</span></span>

## <span data-ttu-id="adccb-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="adccb-127">OUTPUTS</span></span>

### <span data-ttu-id="adccb-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="adccb-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="adccb-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="adccb-129">NOTES</span></span>

## <span data-ttu-id="adccb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adccb-130">RELATED LINKS</span></span>

[<span data-ttu-id="adccb-131">Dodaj-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="adccb-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="adccb-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="adccb-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


