---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524402"
---
# <span data-ttu-id="4506b-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="4506b-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="4506b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4506b-102">SYNOPSIS</span></span>
<span data-ttu-id="4506b-103">Usuwanie zawartości drzwi przednich</span><span class="sxs-lookup"><span data-stu-id="4506b-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4506b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4506b-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4506b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4506b-105">DESCRIPTION</span></span>
<span data-ttu-id="4506b-106">Remove-AzureRmFrontDoorContent Przeczyszcza buforowaną zawartość w przednich drzwiach</span><span class="sxs-lookup"><span data-stu-id="4506b-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="4506b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4506b-107">EXAMPLES</span></span>

### <span data-ttu-id="4506b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4506b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="4506b-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4506b-109">PARAMETERS</span></span>

### <span data-ttu-id="4506b-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="4506b-110">-ContentPath</span></span>
<span data-ttu-id="4506b-111">Ścieżki do zawartości do przeczyszczenia.</span><span class="sxs-lookup"><span data-stu-id="4506b-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="4506b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4506b-112">-DefaultProfile</span></span>
<span data-ttu-id="4506b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4506b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4506b-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4506b-114">-Name</span></span>
<span data-ttu-id="4506b-115">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="4506b-115">Front Door name.</span></span>

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

### <span data-ttu-id="4506b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4506b-116">-PassThru</span></span>
<span data-ttu-id="4506b-117">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="4506b-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="4506b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4506b-118">-ResourceGroupName</span></span>
<span data-ttu-id="4506b-119">Nazwa grupy zasobów dla przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="4506b-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="4506b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4506b-120">-Confirm</span></span>
<span data-ttu-id="4506b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4506b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4506b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4506b-122">-WhatIf</span></span>
<span data-ttu-id="4506b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4506b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4506b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4506b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4506b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4506b-125">CommonParameters</span></span>
<span data-ttu-id="4506b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4506b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4506b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4506b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4506b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4506b-128">INPUTS</span></span>

### <span data-ttu-id="4506b-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4506b-129">None</span></span>

## <span data-ttu-id="4506b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4506b-130">OUTPUTS</span></span>

### <span data-ttu-id="4506b-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4506b-131">System.Boolean</span></span>

## <span data-ttu-id="4506b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4506b-132">NOTES</span></span>

## <span data-ttu-id="4506b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4506b-133">RELATED LINKS</span></span>
