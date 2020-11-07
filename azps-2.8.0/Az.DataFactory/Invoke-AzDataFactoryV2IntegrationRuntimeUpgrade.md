---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: ff2b59310607e360af91e231e09fda60769f0e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706010"
---
# <span data-ttu-id="70548-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="70548-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="70548-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70548-102">SYNOPSIS</span></span>
<span data-ttu-id="70548-103">Uaktualnia środowisko uruchomieniowe integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="70548-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="70548-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70548-104">SYNTAX</span></span>

### <span data-ttu-id="70548-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="70548-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70548-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="70548-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70548-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="70548-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70548-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70548-108">DESCRIPTION</span></span>
<span data-ttu-id="70548-109">Polecenie cmdlet **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** umożliwia uaktualnienie programu obsługi integracji obsługiwanego automatycznie, jeśli jest dostępna nowa wersja.</span><span class="sxs-lookup"><span data-stu-id="70548-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="70548-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70548-110">EXAMPLES</span></span>

### <span data-ttu-id="70548-111">Przykład 1: uaktualnianie samodzielnego środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="70548-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="70548-112">Polecenie cmdlet umożliwia uaktualnienie środowiska wykonawczego integracji obsługiwanego pod nazwą "test-SelfHost-IR" w fabryce danych "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="70548-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="70548-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70548-113">PARAMETERS</span></span>

### <span data-ttu-id="70548-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="70548-114">-DataFactoryName</span></span>
<span data-ttu-id="70548-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="70548-115">The data factory name.</span></span>

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

### <span data-ttu-id="70548-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70548-116">-DefaultProfile</span></span>
<span data-ttu-id="70548-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70548-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70548-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70548-118">-InputObject</span></span>
<span data-ttu-id="70548-119">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="70548-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="70548-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70548-120">-Name</span></span>
<span data-ttu-id="70548-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="70548-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="70548-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70548-122">-ResourceGroupName</span></span>
<span data-ttu-id="70548-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70548-123">The resource group name.</span></span>

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

### <span data-ttu-id="70548-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70548-124">-ResourceId</span></span>
<span data-ttu-id="70548-125">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70548-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="70548-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70548-126">-Confirm</span></span>
<span data-ttu-id="70548-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70548-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70548-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70548-128">-WhatIf</span></span>
<span data-ttu-id="70548-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70548-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70548-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70548-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70548-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70548-131">CommonParameters</span></span>
<span data-ttu-id="70548-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70548-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70548-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70548-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70548-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70548-134">INPUTS</span></span>

### <span data-ttu-id="70548-135">System. String</span><span class="sxs-lookup"><span data-stu-id="70548-135">System.String</span></span>

### <span data-ttu-id="70548-136">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="70548-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="70548-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70548-137">OUTPUTS</span></span>

### <span data-ttu-id="70548-138">System. void</span><span class="sxs-lookup"><span data-stu-id="70548-138">System.Void</span></span>

## <span data-ttu-id="70548-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70548-139">NOTES</span></span>
<span data-ttu-id="70548-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="70548-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="70548-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70548-141">RELATED LINKS</span></span>

<span data-ttu-id="70548-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="70548-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

