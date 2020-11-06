---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: 312ef369e6d191dd96f85a293345d8fa155468b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542679"
---
# <span data-ttu-id="9019e-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="9019e-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="9019e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9019e-102">SYNOPSIS</span></span>
<span data-ttu-id="9019e-103">Uaktualnia środowisko uruchomieniowe integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="9019e-103">Upgrades self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9019e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9019e-104">SYNTAX</span></span>

### <span data-ttu-id="9019e-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9019e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9019e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9019e-106">ByResourceId</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9019e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9019e-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9019e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9019e-108">DESCRIPTION</span></span>
<span data-ttu-id="9019e-109">Polecenie cmdlet **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** umożliwia uaktualnienie programu obsługi integracji obsługiwanego automatycznie, jeśli jest dostępna nowa wersja.</span><span class="sxs-lookup"><span data-stu-id="9019e-109">The **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="9019e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9019e-110">EXAMPLES</span></span>

### <span data-ttu-id="9019e-111">Przykład 1: uaktualnianie samodzielnego środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="9019e-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="9019e-112">Polecenie cmdlet umożliwia uaktualnienie środowiska wykonawczego integracji obsługiwanego pod nazwą "test-SelfHost-IR" w fabryce danych "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="9019e-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="9019e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9019e-113">PARAMETERS</span></span>

### <span data-ttu-id="9019e-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9019e-114">-DataFactoryName</span></span>
<span data-ttu-id="9019e-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="9019e-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9019e-116">-DefaultProfile</span></span>
<span data-ttu-id="9019e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9019e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9019e-118">-InputObject</span></span>
<span data-ttu-id="9019e-119">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="9019e-119">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9019e-120">-Name</span></span>
<span data-ttu-id="9019e-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9019e-121">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9019e-122">-ResourceGroupName</span></span>
<span data-ttu-id="9019e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9019e-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9019e-124">-ResourceId</span></span>
<span data-ttu-id="9019e-125">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9019e-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9019e-126">-Confirm</span></span>
<span data-ttu-id="9019e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9019e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9019e-128">-WhatIf</span></span>
<span data-ttu-id="9019e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9019e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9019e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9019e-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9019e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9019e-131">CommonParameters</span></span>
<span data-ttu-id="9019e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9019e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9019e-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9019e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9019e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9019e-134">INPUTS</span></span>

### <span data-ttu-id="9019e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9019e-135">System.String</span></span>
<span data-ttu-id="9019e-136">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9019e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9019e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9019e-137">OUTPUTS</span></span>

### <span data-ttu-id="9019e-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="9019e-138">System.Object</span></span>

## <span data-ttu-id="9019e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9019e-139">NOTES</span></span>
<span data-ttu-id="9019e-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="9019e-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="9019e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9019e-141">RELATED LINKS</span></span>

<span data-ttu-id="9019e-142">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="9019e-142">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

