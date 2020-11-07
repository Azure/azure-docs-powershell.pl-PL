---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896342"
---
# <span data-ttu-id="b3feb-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b3feb-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="b3feb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3feb-102">SYNOPSIS</span></span>
<span data-ttu-id="b3feb-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="b3feb-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="b3feb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3feb-104">SYNTAX</span></span>

### <span data-ttu-id="b3feb-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3feb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3feb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3feb-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3feb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b3feb-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3feb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b3feb-108">DESCRIPTION</span></span>
<span data-ttu-id="b3feb-109">Polecenie cmdlet Remove-AzDataFactoryV2IntegrationRuntime usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="b3feb-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="b3feb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3feb-110">EXAMPLES</span></span>

### <span data-ttu-id="b3feb-111">Przykład 1: usuwanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="b3feb-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="b3feb-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie test-zastrzeżonym-IR ' z fabryki danych o nazwie test-DF.</span><span class="sxs-lookup"><span data-stu-id="b3feb-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="b3feb-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="b3feb-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="b3feb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3feb-114">PARAMETERS</span></span>

### <span data-ttu-id="b3feb-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b3feb-115">-DataFactoryName</span></span>
<span data-ttu-id="b3feb-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="b3feb-116">The data factory name.</span></span>

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

### <span data-ttu-id="b3feb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3feb-117">-DefaultProfile</span></span>
<span data-ttu-id="b3feb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3feb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3feb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b3feb-119">-Force</span></span>
<span data-ttu-id="b3feb-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3feb-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b3feb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3feb-121">-InputObject</span></span>
<span data-ttu-id="b3feb-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="b3feb-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="b3feb-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b3feb-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="b3feb-124">Nazwa fabryki danych połączonych.</span><span class="sxs-lookup"><span data-stu-id="b3feb-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="b3feb-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3feb-125">-Name</span></span>
<span data-ttu-id="b3feb-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="b3feb-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="b3feb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3feb-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3feb-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3feb-128">The resource group name.</span></span>

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

### <span data-ttu-id="b3feb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3feb-129">-ResourceId</span></span>
<span data-ttu-id="b3feb-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3feb-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b3feb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3feb-131">-Confirm</span></span>
<span data-ttu-id="b3feb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3feb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3feb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3feb-133">-WhatIf</span></span>
<span data-ttu-id="b3feb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3feb-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b3feb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3feb-135">CommonParameters</span></span>
<span data-ttu-id="b3feb-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3feb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3feb-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3feb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3feb-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3feb-138">INPUTS</span></span>

### <span data-ttu-id="b3feb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b3feb-139">System.String</span></span>

### <span data-ttu-id="b3feb-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b3feb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b3feb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3feb-141">OUTPUTS</span></span>

### <span data-ttu-id="b3feb-142">System. void</span><span class="sxs-lookup"><span data-stu-id="b3feb-142">System.Void</span></span>

## <span data-ttu-id="b3feb-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3feb-143">NOTES</span></span>
<span data-ttu-id="b3feb-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="b3feb-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b3feb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3feb-145">RELATED LINKS</span></span>

[<span data-ttu-id="b3feb-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b3feb-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="b3feb-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b3feb-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

