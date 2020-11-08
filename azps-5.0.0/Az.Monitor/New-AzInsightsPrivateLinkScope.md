---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233332"
---
# <span data-ttu-id="8eddf-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="8eddf-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="8eddf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8eddf-102">SYNOPSIS</span></span>
<span data-ttu-id="8eddf-103">Tworzenie prywatnego zakresu linków</span><span class="sxs-lookup"><span data-stu-id="8eddf-103">create private link scope</span></span>

## <span data-ttu-id="8eddf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8eddf-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eddf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8eddf-105">DESCRIPTION</span></span>
<span data-ttu-id="8eddf-106">Tworzenie prywatnego zakresu linków</span><span class="sxs-lookup"><span data-stu-id="8eddf-106">create private link scope</span></span>

## <span data-ttu-id="8eddf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8eddf-107">EXAMPLES</span></span>

### <span data-ttu-id="8eddf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8eddf-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="8eddf-109">Tworzenie prywatnego zakresu linków o nazwie "scope_name" w grupie zasób "rg_name" w lokalizacji "Wschód"</span><span class="sxs-lookup"><span data-stu-id="8eddf-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="8eddf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8eddf-110">PARAMETERS</span></span>

### <span data-ttu-id="8eddf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eddf-111">-DefaultProfile</span></span>
<span data-ttu-id="8eddf-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8eddf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eddf-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8eddf-113">-Location</span></span>
<span data-ttu-id="8eddf-114">Pozycję</span><span class="sxs-lookup"><span data-stu-id="8eddf-114">Location</span></span>

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

### <span data-ttu-id="8eddf-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8eddf-115">-Name</span></span>
<span data-ttu-id="8eddf-116">Nazwa zakresu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="8eddf-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="8eddf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eddf-117">-ResourceGroupName</span></span>
<span data-ttu-id="8eddf-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8eddf-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8eddf-119">-Tagi</span><span class="sxs-lookup"><span data-stu-id="8eddf-119">-Tags</span></span>
<span data-ttu-id="8eddf-120">Kolczyk</span><span class="sxs-lookup"><span data-stu-id="8eddf-120">Tags</span></span>

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

### <span data-ttu-id="8eddf-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8eddf-121">-Confirm</span></span>
<span data-ttu-id="8eddf-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eddf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eddf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eddf-123">-WhatIf</span></span>
<span data-ttu-id="8eddf-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eddf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eddf-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8eddf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eddf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eddf-126">CommonParameters</span></span>
<span data-ttu-id="8eddf-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eddf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eddf-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8eddf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eddf-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8eddf-129">INPUTS</span></span>

### <span data-ttu-id="8eddf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8eddf-130">System.String</span></span>

## <span data-ttu-id="8eddf-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8eddf-131">OUTPUTS</span></span>

### <span data-ttu-id="8eddf-132">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="8eddf-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="8eddf-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8eddf-133">NOTES</span></span>

## <span data-ttu-id="8eddf-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8eddf-134">RELATED LINKS</span></span>
