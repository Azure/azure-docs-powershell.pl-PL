---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: f48dedc50ae134967a57320b065389505aa9c1ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868360"
---
# <span data-ttu-id="d0946-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="d0946-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="d0946-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0946-102">SYNOPSIS</span></span>
<span data-ttu-id="d0946-103">Usuwanie zawartości drzwi przednich</span><span class="sxs-lookup"><span data-stu-id="d0946-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="d0946-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0946-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0946-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0946-105">DESCRIPTION</span></span>
<span data-ttu-id="d0946-106">Remove-AzFrontDoorContent Przeczyszcza buforowaną zawartość w przednich drzwiach</span><span class="sxs-lookup"><span data-stu-id="d0946-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="d0946-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0946-107">EXAMPLES</span></span>

### <span data-ttu-id="d0946-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0946-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="d0946-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0946-109">PARAMETERS</span></span>

### <span data-ttu-id="d0946-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="d0946-110">-ContentPath</span></span>
<span data-ttu-id="d0946-111">Ścieżki do zawartości do przeczyszczenia.</span><span class="sxs-lookup"><span data-stu-id="d0946-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0946-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0946-112">-DefaultProfile</span></span>
<span data-ttu-id="d0946-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0946-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0946-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0946-114">-Name</span></span>
<span data-ttu-id="d0946-115">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="d0946-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0946-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0946-116">-PassThru</span></span>
<span data-ttu-id="d0946-117">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="d0946-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="d0946-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0946-118">-ResourceGroupName</span></span>
<span data-ttu-id="d0946-119">Nazwa grupy zasobów dla przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="d0946-119">The resource group name of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0946-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0946-120">-Confirm</span></span>
<span data-ttu-id="d0946-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0946-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0946-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0946-122">-WhatIf</span></span>
<span data-ttu-id="d0946-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0946-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0946-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0946-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0946-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0946-125">CommonParameters</span></span>
<span data-ttu-id="d0946-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0946-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0946-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0946-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0946-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0946-128">INPUTS</span></span>

### <span data-ttu-id="d0946-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0946-129">None</span></span>

## <span data-ttu-id="d0946-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0946-130">OUTPUTS</span></span>

### <span data-ttu-id="d0946-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0946-131">System.Boolean</span></span>

## <span data-ttu-id="d0946-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0946-132">NOTES</span></span>

## <span data-ttu-id="d0946-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0946-133">RELATED LINKS</span></span>
