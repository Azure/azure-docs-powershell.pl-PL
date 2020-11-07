---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 9478c190d33608706006ff7fe792b4ee8f14b9d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705964"
---
# <span data-ttu-id="be166-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be166-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="be166-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be166-102">SYNOPSIS</span></span>
<span data-ttu-id="be166-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="be166-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="be166-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be166-104">SYNTAX</span></span>

### <span data-ttu-id="be166-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be166-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be166-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be166-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be166-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="be166-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be166-108">Opis</span><span class="sxs-lookup"><span data-stu-id="be166-108">DESCRIPTION</span></span>
<span data-ttu-id="be166-109">Polecenie cmdlet Remove-AzDataFactoryV2IntegrationRuntime usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="be166-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="be166-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be166-110">EXAMPLES</span></span>

### <span data-ttu-id="be166-111">Przykład 1: usuwanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="be166-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="be166-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie test-zastrzeżonym-IR ' z fabryki danych o nazwie test-DF.</span><span class="sxs-lookup"><span data-stu-id="be166-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="be166-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="be166-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="be166-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be166-114">PARAMETERS</span></span>

### <span data-ttu-id="be166-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="be166-115">-DataFactoryName</span></span>
<span data-ttu-id="be166-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="be166-116">The data factory name.</span></span>

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

### <span data-ttu-id="be166-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be166-117">-DefaultProfile</span></span>
<span data-ttu-id="be166-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be166-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be166-119">-Force</span><span class="sxs-lookup"><span data-stu-id="be166-119">-Force</span></span>
<span data-ttu-id="be166-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be166-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="be166-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="be166-121">-InputObject</span></span>
<span data-ttu-id="be166-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="be166-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="be166-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="be166-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="be166-124">Nazwa fabryki danych połączonych.</span><span class="sxs-lookup"><span data-stu-id="be166-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="be166-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be166-125">-Name</span></span>
<span data-ttu-id="be166-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="be166-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="be166-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be166-127">-ResourceGroupName</span></span>
<span data-ttu-id="be166-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="be166-128">The resource group name.</span></span>

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

### <span data-ttu-id="be166-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be166-129">-ResourceId</span></span>
<span data-ttu-id="be166-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be166-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="be166-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be166-131">-Confirm</span></span>
<span data-ttu-id="be166-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be166-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be166-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be166-133">-WhatIf</span></span>
<span data-ttu-id="be166-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be166-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="be166-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be166-135">CommonParameters</span></span>
<span data-ttu-id="be166-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be166-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be166-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be166-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be166-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be166-138">INPUTS</span></span>

### <span data-ttu-id="be166-139">System. String</span><span class="sxs-lookup"><span data-stu-id="be166-139">System.String</span></span>

### <span data-ttu-id="be166-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be166-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="be166-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be166-141">OUTPUTS</span></span>

### <span data-ttu-id="be166-142">System. void</span><span class="sxs-lookup"><span data-stu-id="be166-142">System.Void</span></span>

## <span data-ttu-id="be166-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be166-143">NOTES</span></span>
<span data-ttu-id="be166-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="be166-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="be166-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be166-145">RELATED LINKS</span></span>

[<span data-ttu-id="be166-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be166-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="be166-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be166-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

