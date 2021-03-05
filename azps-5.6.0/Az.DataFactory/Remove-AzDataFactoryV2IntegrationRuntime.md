---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 72b00b855bcc50df2766a6b8d0315780aaa64ecf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009665"
---
# <span data-ttu-id="6a0be-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a0be-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6a0be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a0be-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0be-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="6a0be-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="6a0be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a0be-104">SYNTAX</span></span>

### <span data-ttu-id="6a0be-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6a0be-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a0be-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a0be-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a0be-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6a0be-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a0be-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a0be-108">DESCRIPTION</span></span>
<span data-ttu-id="6a0be-109">To Remove-AzDataFactoryV2IntegrationRuntime cmdlet usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="6a0be-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="6a0be-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a0be-110">EXAMPLES</span></span>

### <span data-ttu-id="6a0be-111">Przykład 1. Usuwanie środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="6a0be-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="6a0be-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie "test-reserved-ir" z fabryki danych o nazwie "test-df".</span><span class="sxs-lookup"><span data-stu-id="6a0be-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="6a0be-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="6a0be-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="6a0be-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a0be-114">PARAMETERS</span></span>

### <span data-ttu-id="6a0be-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6a0be-115">-DataFactoryName</span></span>
<span data-ttu-id="6a0be-116">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="6a0be-116">The data factory name.</span></span>

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

### <span data-ttu-id="6a0be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0be-117">-DefaultProfile</span></span>
<span data-ttu-id="6a0be-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0be-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a0be-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6a0be-119">-Force</span></span>
<span data-ttu-id="6a0be-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a0be-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6a0be-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a0be-121">-InputObject</span></span>
<span data-ttu-id="6a0be-122">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6a0be-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="6a0be-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6a0be-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="6a0be-124">Nazwa połączonej fabrycznej usługi danych.</span><span class="sxs-lookup"><span data-stu-id="6a0be-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="6a0be-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6a0be-125">-Name</span></span>
<span data-ttu-id="6a0be-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6a0be-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="6a0be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0be-127">-ResourceGroupName</span></span>
<span data-ttu-id="6a0be-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a0be-128">The resource group name.</span></span>

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

### <span data-ttu-id="6a0be-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a0be-129">-ResourceId</span></span>
<span data-ttu-id="6a0be-130">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0be-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6a0be-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a0be-131">-Confirm</span></span>
<span data-ttu-id="6a0be-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a0be-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a0be-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0be-133">-WhatIf</span></span>
<span data-ttu-id="6a0be-134">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a0be-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6a0be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0be-135">CommonParameters</span></span>
<span data-ttu-id="6a0be-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a0be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0be-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a0be-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0be-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a0be-138">INPUTS</span></span>

### <span data-ttu-id="6a0be-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6a0be-139">System.String</span></span>

### <span data-ttu-id="6a0be-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a0be-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6a0be-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a0be-141">OUTPUTS</span></span>

### <span data-ttu-id="6a0be-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a0be-142">System.Void</span></span>

## <span data-ttu-id="6a0be-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a0be-143">NOTES</span></span>
<span data-ttu-id="6a0be-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="6a0be-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="6a0be-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a0be-145">RELATED LINKS</span></span>

[<span data-ttu-id="6a0be-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a0be-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="6a0be-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a0be-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

