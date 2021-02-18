---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180987"
---
# <span data-ttu-id="d2e04-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d2e04-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="d2e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e04-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e04-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="d2e04-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="d2e04-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2e04-104">SYNTAX</span></span>

### <span data-ttu-id="d2e04-105">ByIntegrationRuntimeName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d2e04-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e04-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e04-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e04-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d2e04-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2e04-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2e04-108">DESCRIPTION</span></span>
<span data-ttu-id="d2e04-109">To Remove-AzDataFactoryV2IntegrationRuntime cmdlet usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="d2e04-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="d2e04-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2e04-110">EXAMPLES</span></span>

### <span data-ttu-id="d2e04-111">Przykład 1. Usuwanie środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="d2e04-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="d2e04-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie "test-reserved-ir" z fabryki danych o nazwie "test-df".</span><span class="sxs-lookup"><span data-stu-id="d2e04-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="d2e04-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="d2e04-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="d2e04-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2e04-114">PARAMETERS</span></span>

### <span data-ttu-id="d2e04-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d2e04-115">-DataFactoryName</span></span>
<span data-ttu-id="d2e04-116">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="d2e04-116">The data factory name.</span></span>

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

### <span data-ttu-id="d2e04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e04-117">-DefaultProfile</span></span>
<span data-ttu-id="d2e04-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e04-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e04-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d2e04-119">-Force</span></span>
<span data-ttu-id="d2e04-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2e04-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d2e04-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e04-121">-InputObject</span></span>
<span data-ttu-id="d2e04-122">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="d2e04-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="d2e04-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d2e04-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="d2e04-124">Nazwa połączonej fabrycznej usługi danych.</span><span class="sxs-lookup"><span data-stu-id="d2e04-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e04-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2e04-125">-Name</span></span>
<span data-ttu-id="d2e04-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="d2e04-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="d2e04-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e04-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2e04-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2e04-128">The resource group name.</span></span>

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

### <span data-ttu-id="d2e04-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e04-129">-ResourceId</span></span>
<span data-ttu-id="d2e04-130">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e04-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d2e04-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2e04-131">-Confirm</span></span>
<span data-ttu-id="d2e04-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2e04-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e04-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e04-133">-WhatIf</span></span>
<span data-ttu-id="d2e04-134">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2e04-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d2e04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e04-135">CommonParameters</span></span>
<span data-ttu-id="d2e04-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e04-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e04-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e04-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2e04-138">INPUTS</span></span>

### <span data-ttu-id="d2e04-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d2e04-139">System.String</span></span>

### <span data-ttu-id="d2e04-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d2e04-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d2e04-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2e04-141">OUTPUTS</span></span>

### <span data-ttu-id="d2e04-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="d2e04-142">System.Void</span></span>

## <span data-ttu-id="d2e04-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2e04-143">NOTES</span></span>
<span data-ttu-id="d2e04-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="d2e04-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="d2e04-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2e04-145">RELATED LINKS</span></span>

[<span data-ttu-id="d2e04-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d2e04-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="d2e04-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d2e04-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

