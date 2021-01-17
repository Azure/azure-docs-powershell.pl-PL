---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381255"
---
# <span data-ttu-id="0406a-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0406a-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="0406a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0406a-102">SYNOPSIS</span></span>
<span data-ttu-id="0406a-103">Usuwanie konta połączonego magazynu z aplikacją Application Insights</span><span class="sxs-lookup"><span data-stu-id="0406a-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="0406a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0406a-104">SYNTAX</span></span>

### <span data-ttu-id="0406a-105">ByResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0406a-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0406a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0406a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0406a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0406a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0406a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0406a-108">DESCRIPTION</span></span>
<span data-ttu-id="0406a-109">Usuwanie konta połączonego magazynu z aplikacją Application Insights</span><span class="sxs-lookup"><span data-stu-id="0406a-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="0406a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0406a-110">EXAMPLES</span></span>

### <span data-ttu-id="0406a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0406a-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="0406a-112">Usuwanie połączonego konta magazynu skojarzonego z składnikiem usługi Application Insights "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="0406a-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="0406a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0406a-113">PARAMETERS</span></span>

### <span data-ttu-id="0406a-114">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="0406a-114">-ComponentName</span></span>
<span data-ttu-id="0406a-115">Nazwa składnika</span><span class="sxs-lookup"><span data-stu-id="0406a-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0406a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0406a-116">-DefaultProfile</span></span>
<span data-ttu-id="0406a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0406a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0406a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0406a-118">-InputObject</span></span>
<span data-ttu-id="0406a-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0406a-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0406a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0406a-120">-ResourceGroupName</span></span>
<span data-ttu-id="0406a-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0406a-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0406a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0406a-122">-ResourceId</span></span>
<span data-ttu-id="0406a-123">Identyfikator zasobu składnika</span><span class="sxs-lookup"><span data-stu-id="0406a-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0406a-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0406a-124">-Confirm</span></span>
<span data-ttu-id="0406a-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0406a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0406a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0406a-126">-WhatIf</span></span>
<span data-ttu-id="0406a-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0406a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0406a-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0406a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0406a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0406a-129">CommonParameters</span></span>
<span data-ttu-id="0406a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0406a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0406a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0406a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0406a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0406a-132">INPUTS</span></span>

### <span data-ttu-id="0406a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0406a-133">System.String</span></span>

### <span data-ttu-id="0406a-134">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0406a-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="0406a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0406a-135">OUTPUTS</span></span>

### <span data-ttu-id="0406a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0406a-136">System.Boolean</span></span>

## <span data-ttu-id="0406a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0406a-137">NOTES</span></span>

## <span data-ttu-id="0406a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0406a-138">RELATED LINKS</span></span>
