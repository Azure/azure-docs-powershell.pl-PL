---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232615"
---
# <span data-ttu-id="9e0cd-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e0cd-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="9e0cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0cd-103">Tworzenie konta połączonego magazynu z aplikacją Application Insights</span><span class="sxs-lookup"><span data-stu-id="9e0cd-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="9e0cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e0cd-104">SYNTAX</span></span>

### <span data-ttu-id="9e0cd-105">ByResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e0cd-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e0cd-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e0cd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e0cd-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e0cd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9e0cd-108">DESCRIPTION</span></span>
<span data-ttu-id="9e0cd-109">Tworzenie konta połączonego magazynu z aplikacją Application Insights</span><span class="sxs-lookup"><span data-stu-id="9e0cd-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="9e0cd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e0cd-110">EXAMPLES</span></span>

### <span data-ttu-id="9e0cd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e0cd-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="9e0cd-112">Tworzenie połączonego konta magazynu $account w obszarze składnik "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="9e0cd-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="9e0cd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e0cd-113">PARAMETERS</span></span>

### <span data-ttu-id="9e0cd-114">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="9e0cd-114">-ComponentName</span></span>
<span data-ttu-id="9e0cd-115">Nazwa składnika</span><span class="sxs-lookup"><span data-stu-id="9e0cd-115">Component Name</span></span>

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

### <span data-ttu-id="9e0cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0cd-116">-DefaultProfile</span></span>
<span data-ttu-id="9e0cd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e0cd-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e0cd-118">-InputObject</span></span>
<span data-ttu-id="9e0cd-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9e0cd-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="9e0cd-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9e0cd-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="9e0cd-121">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9e0cd-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="9e0cd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e0cd-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e0cd-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9e0cd-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9e0cd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e0cd-124">-ResourceId</span></span>
<span data-ttu-id="9e0cd-125">Identyfikator zasobu składnika</span><span class="sxs-lookup"><span data-stu-id="9e0cd-125">Component ResourceId</span></span>

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

### <span data-ttu-id="9e0cd-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e0cd-126">-Confirm</span></span>
<span data-ttu-id="9e0cd-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e0cd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e0cd-128">-WhatIf</span></span>
<span data-ttu-id="9e0cd-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e0cd-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e0cd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0cd-131">CommonParameters</span></span>
<span data-ttu-id="9e0cd-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0cd-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e0cd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0cd-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e0cd-134">INPUTS</span></span>

### <span data-ttu-id="9e0cd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9e0cd-135">System.String</span></span>

### <span data-ttu-id="9e0cd-136">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9e0cd-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="9e0cd-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e0cd-137">OUTPUTS</span></span>

### <span data-ttu-id="9e0cd-138">Microsoft. Azure. Commands. ApplicationInsights. models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="9e0cd-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="9e0cd-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e0cd-139">NOTES</span></span>

## <span data-ttu-id="9e0cd-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e0cd-140">RELATED LINKS</span></span>
