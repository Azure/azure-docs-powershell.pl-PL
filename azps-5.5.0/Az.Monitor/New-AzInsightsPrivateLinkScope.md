---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180130"
---
# <span data-ttu-id="e0a20-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e0a20-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="e0a20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a20-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a20-103">Tworzenie prywatnego zakresu łączy</span><span class="sxs-lookup"><span data-stu-id="e0a20-103">create private link scope</span></span>

## <span data-ttu-id="e0a20-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0a20-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0a20-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0a20-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a20-106">Tworzenie zakresu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="e0a20-106">create private link scope</span></span>

## <span data-ttu-id="e0a20-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0a20-107">EXAMPLES</span></span>

### <span data-ttu-id="e0a20-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0a20-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="e0a20-109">Tworzenie prywatnego zakresu łączy o nazwie "scope_name" w grupie zasobów "rg_name" w lokalizacji "eastus"</span><span class="sxs-lookup"><span data-stu-id="e0a20-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="e0a20-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0a20-110">PARAMETERS</span></span>

### <span data-ttu-id="e0a20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a20-111">-DefaultProfile</span></span>
<span data-ttu-id="e0a20-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0a20-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0a20-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e0a20-113">-Location</span></span>
<span data-ttu-id="e0a20-114">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e0a20-114">Location</span></span>

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

### <span data-ttu-id="e0a20-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0a20-115">-Name</span></span>
<span data-ttu-id="e0a20-116">Nazwa zakresu łącza prywatnego</span><span class="sxs-lookup"><span data-stu-id="e0a20-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="e0a20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a20-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0a20-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e0a20-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e0a20-119">— Tagi</span><span class="sxs-lookup"><span data-stu-id="e0a20-119">-Tags</span></span>
<span data-ttu-id="e0a20-120">Tagi</span><span class="sxs-lookup"><span data-stu-id="e0a20-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a20-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0a20-121">-Confirm</span></span>
<span data-ttu-id="e0a20-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0a20-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0a20-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0a20-123">-WhatIf</span></span>
<span data-ttu-id="e0a20-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0a20-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0a20-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0a20-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0a20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a20-126">CommonParameters</span></span>
<span data-ttu-id="e0a20-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0a20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a20-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0a20-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a20-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0a20-129">INPUTS</span></span>

### <span data-ttu-id="e0a20-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e0a20-130">System.String</span></span>

## <span data-ttu-id="e0a20-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0a20-131">OUTPUTS</span></span>

### <span data-ttu-id="e0a20-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e0a20-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="e0a20-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0a20-133">NOTES</span></span>

## <span data-ttu-id="e0a20-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0a20-134">RELATED LINKS</span></span>
