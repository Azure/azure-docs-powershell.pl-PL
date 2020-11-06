---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 05b9c5bce3158413f562c38eb116523609696523
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545395"
---
# <span data-ttu-id="bda4e-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="bda4e-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="bda4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bda4e-102">SYNOPSIS</span></span>
<span data-ttu-id="bda4e-103">Synchronizuje poświadczenia między węzłami w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="bda4e-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bda4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bda4e-104">SYNTAX</span></span>

### <span data-ttu-id="bda4e-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bda4e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bda4e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bda4e-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bda4e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="bda4e-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bda4e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bda4e-108">DESCRIPTION</span></span>
<span data-ttu-id="bda4e-109">Polecenie cmdlet **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** synchronizuje poświadczenia lokalne między węzłami środowiska wykonawczego programu integracyjnego, które wymuszają identyczne poświadczenia we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="bda4e-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="bda4e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bda4e-110">EXAMPLES</span></span>

### <span data-ttu-id="bda4e-111">Przykład 1: synchronizowanie poświadczenia środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="bda4e-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="bda4e-112">Polecenie cmdlet synchronizuje poświadczenia między węzłami środowiska wykonawczego programu integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="bda4e-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="bda4e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bda4e-113">PARAMETERS</span></span>

### <span data-ttu-id="bda4e-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bda4e-114">-DataFactoryName</span></span>
<span data-ttu-id="bda4e-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bda4e-115">The data factory name.</span></span>

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

### <span data-ttu-id="bda4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda4e-116">-DefaultProfile</span></span>
<span data-ttu-id="bda4e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bda4e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bda4e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bda4e-118">-Force</span></span>
<span data-ttu-id="bda4e-119">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bda4e-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="bda4e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bda4e-120">-InputObject</span></span>
<span data-ttu-id="bda4e-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="bda4e-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="bda4e-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="bda4e-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="bda4e-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="bda4e-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda4e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda4e-124">-ResourceGroupName</span></span>
<span data-ttu-id="bda4e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bda4e-125">The resource group name.</span></span>

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

### <span data-ttu-id="bda4e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bda4e-126">-ResourceId</span></span>
<span data-ttu-id="bda4e-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bda4e-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bda4e-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bda4e-128">-Confirm</span></span>
<span data-ttu-id="bda4e-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bda4e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bda4e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bda4e-130">-WhatIf</span></span>
<span data-ttu-id="bda4e-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bda4e-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="bda4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda4e-132">CommonParameters</span></span>
<span data-ttu-id="bda4e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda4e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda4e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda4e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bda4e-135">INPUTS</span></span>

### <span data-ttu-id="bda4e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bda4e-136">System.String</span></span>

### <span data-ttu-id="bda4e-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bda4e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="bda4e-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bda4e-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bda4e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bda4e-139">OUTPUTS</span></span>

### <span data-ttu-id="bda4e-140">System. void</span><span class="sxs-lookup"><span data-stu-id="bda4e-140">System.Void</span></span>

## <span data-ttu-id="bda4e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bda4e-141">NOTES</span></span>

## <span data-ttu-id="bda4e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bda4e-142">RELATED LINKS</span></span>
