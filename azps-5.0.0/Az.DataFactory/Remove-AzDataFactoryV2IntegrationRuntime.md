---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306090"
---
# <span data-ttu-id="98d6b-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="98d6b-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="98d6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="98d6b-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="98d6b-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="98d6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98d6b-104">SYNTAX</span></span>

### <span data-ttu-id="98d6b-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98d6b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98d6b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98d6b-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98d6b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="98d6b-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98d6b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="98d6b-108">DESCRIPTION</span></span>
<span data-ttu-id="98d6b-109">Polecenie cmdlet Remove-AzDataFactoryV2IntegrationRuntime usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="98d6b-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="98d6b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98d6b-110">EXAMPLES</span></span>

### <span data-ttu-id="98d6b-111">Przykład 1: usuwanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="98d6b-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="98d6b-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie test-zastrzeżonym-IR ' z fabryki danych o nazwie test-DF.</span><span class="sxs-lookup"><span data-stu-id="98d6b-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="98d6b-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="98d6b-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="98d6b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98d6b-114">PARAMETERS</span></span>

### <span data-ttu-id="98d6b-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="98d6b-115">-DataFactoryName</span></span>
<span data-ttu-id="98d6b-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="98d6b-116">The data factory name.</span></span>

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

### <span data-ttu-id="98d6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d6b-117">-DefaultProfile</span></span>
<span data-ttu-id="98d6b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98d6b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d6b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="98d6b-119">-Force</span></span>
<span data-ttu-id="98d6b-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98d6b-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="98d6b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98d6b-121">-InputObject</span></span>
<span data-ttu-id="98d6b-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="98d6b-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="98d6b-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="98d6b-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="98d6b-124">Nazwa fabryki danych połączonych.</span><span class="sxs-lookup"><span data-stu-id="98d6b-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="98d6b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98d6b-125">-Name</span></span>
<span data-ttu-id="98d6b-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="98d6b-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="98d6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="98d6b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98d6b-128">The resource group name.</span></span>

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

### <span data-ttu-id="98d6b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98d6b-129">-ResourceId</span></span>
<span data-ttu-id="98d6b-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98d6b-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="98d6b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98d6b-131">-Confirm</span></span>
<span data-ttu-id="98d6b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d6b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d6b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d6b-133">-WhatIf</span></span>
<span data-ttu-id="98d6b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d6b-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="98d6b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d6b-135">CommonParameters</span></span>
<span data-ttu-id="98d6b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d6b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d6b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98d6b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d6b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98d6b-138">INPUTS</span></span>

### <span data-ttu-id="98d6b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="98d6b-139">System.String</span></span>

### <span data-ttu-id="98d6b-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="98d6b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="98d6b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98d6b-141">OUTPUTS</span></span>

### <span data-ttu-id="98d6b-142">System. void</span><span class="sxs-lookup"><span data-stu-id="98d6b-142">System.Void</span></span>

## <span data-ttu-id="98d6b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98d6b-143">NOTES</span></span>
<span data-ttu-id="98d6b-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="98d6b-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="98d6b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98d6b-145">RELATED LINKS</span></span>

[<span data-ttu-id="98d6b-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="98d6b-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="98d6b-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="98d6b-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

