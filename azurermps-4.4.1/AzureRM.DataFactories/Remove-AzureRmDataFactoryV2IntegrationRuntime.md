---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: bf29e12292fba12cc6a5b4f99cef1e13f9d9fd8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548303"
---
# <span data-ttu-id="58490-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58490-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="58490-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58490-102">SYNOPSIS</span></span>
<span data-ttu-id="58490-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="58490-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58490-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58490-104">SYNTAX</span></span>

### <span data-ttu-id="58490-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58490-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58490-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="58490-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58490-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="58490-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58490-108">Opis</span><span class="sxs-lookup"><span data-stu-id="58490-108">DESCRIPTION</span></span>
<span data-ttu-id="58490-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="58490-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="58490-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58490-110">EXAMPLES</span></span>

### <span data-ttu-id="58490-111">Przykład 1: usuwanie środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="58490-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="58490-112">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie test-zastrzeżonym-IR ' z fabryki danych o nazwie test-DF.</span><span class="sxs-lookup"><span data-stu-id="58490-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="58490-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="58490-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="58490-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58490-114">PARAMETERS</span></span>

### <span data-ttu-id="58490-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="58490-115">-DataFactoryName</span></span>
<span data-ttu-id="58490-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="58490-116">The data factory name.</span></span>

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

### <span data-ttu-id="58490-117">-Force</span><span class="sxs-lookup"><span data-stu-id="58490-117">-Force</span></span>
<span data-ttu-id="58490-118">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58490-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="58490-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="58490-119">-InputObject</span></span>
<span data-ttu-id="58490-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="58490-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="58490-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58490-121">-Name</span></span>
<span data-ttu-id="58490-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="58490-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="58490-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58490-123">-ResourceGroupName</span></span>
<span data-ttu-id="58490-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58490-124">The resource group name.</span></span>

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

### <span data-ttu-id="58490-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58490-125">-ResourceId</span></span>
<span data-ttu-id="58490-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="58490-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="58490-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58490-127">-Confirm</span></span>
<span data-ttu-id="58490-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58490-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58490-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58490-129">-WhatIf</span></span>
<span data-ttu-id="58490-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58490-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="58490-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58490-131">-DefaultProfile</span></span>
<span data-ttu-id="58490-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58490-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58490-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58490-133">CommonParameters</span></span>
<span data-ttu-id="58490-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58490-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58490-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58490-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58490-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58490-136">INPUTS</span></span>

### <span data-ttu-id="58490-137">System. String</span><span class="sxs-lookup"><span data-stu-id="58490-137">System.String</span></span>
<span data-ttu-id="58490-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58490-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="58490-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58490-139">OUTPUTS</span></span>

### <span data-ttu-id="58490-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="58490-140">System.Object</span></span>

## <span data-ttu-id="58490-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58490-141">NOTES</span></span>
<span data-ttu-id="58490-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="58490-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="58490-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58490-143">RELATED LINKS</span></span>

[<span data-ttu-id="58490-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58490-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="58490-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58490-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

