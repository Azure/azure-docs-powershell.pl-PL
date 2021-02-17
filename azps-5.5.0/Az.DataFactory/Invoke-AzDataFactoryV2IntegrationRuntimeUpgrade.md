---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177163"
---
# <span data-ttu-id="c2554-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="c2554-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="c2554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2554-102">SYNOPSIS</span></span>
<span data-ttu-id="c2554-103">Uaktualnienie środowiska integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="c2554-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="c2554-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2554-104">SYNTAX</span></span>

### <span data-ttu-id="c2554-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c2554-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2554-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2554-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2554-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c2554-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2554-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2554-108">DESCRIPTION</span></span>
<span data-ttu-id="c2554-109">Polecenie cmdlet **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** uaktualni środowisko uruchomieniowe integracji samoobsługowej, jeśli jest dostępna nowa wersja.</span><span class="sxs-lookup"><span data-stu-id="c2554-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="c2554-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2554-110">EXAMPLES</span></span>

### <span data-ttu-id="c2554-111">Przykład 1. Uaktualnienie środowiska integracji z własnym hostem</span><span class="sxs-lookup"><span data-stu-id="c2554-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="c2554-112">Polecenie cmdlet uaktualnia środowisko uruchomieniowe integracji z własnym hostem o nazwie "test-selfhost-ir" w środowisku data factory 'test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="c2554-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="c2554-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2554-113">PARAMETERS</span></span>

### <span data-ttu-id="c2554-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c2554-114">-DataFactoryName</span></span>
<span data-ttu-id="c2554-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="c2554-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2554-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2554-116">-DefaultProfile</span></span>
<span data-ttu-id="c2554-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2554-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2554-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2554-118">-InputObject</span></span>
<span data-ttu-id="c2554-119">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c2554-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2554-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c2554-120">-Name</span></span>
<span data-ttu-id="c2554-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c2554-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2554-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2554-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2554-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2554-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2554-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2554-124">-ResourceId</span></span>
<span data-ttu-id="c2554-125">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="c2554-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2554-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2554-126">-Confirm</span></span>
<span data-ttu-id="c2554-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2554-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2554-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2554-128">-WhatIf</span></span>
<span data-ttu-id="c2554-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2554-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2554-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2554-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2554-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2554-131">CommonParameters</span></span>
<span data-ttu-id="c2554-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2554-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2554-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2554-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2554-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2554-134">INPUTS</span></span>

### <span data-ttu-id="c2554-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c2554-135">System.String</span></span>

### <span data-ttu-id="c2554-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c2554-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c2554-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2554-137">OUTPUTS</span></span>

### <span data-ttu-id="c2554-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="c2554-138">System.Void</span></span>

## <span data-ttu-id="c2554-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2554-139">NOTES</span></span>
<span data-ttu-id="c2554-140">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="c2554-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c2554-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2554-141">RELATED LINKS</span></span>

<span data-ttu-id="c2554-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="c2554-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

