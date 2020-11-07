---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716695"
---
# <span data-ttu-id="54c33-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="54c33-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="54c33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54c33-102">SYNOPSIS</span></span>
<span data-ttu-id="54c33-103">Synchronizuje poświadczenia między węzłami w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="54c33-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54c33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54c33-104">SYNTAX</span></span>

### <span data-ttu-id="54c33-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="54c33-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="54c33-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="54c33-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="54c33-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="54c33-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="54c33-108">Opis</span><span class="sxs-lookup"><span data-stu-id="54c33-108">DESCRIPTION</span></span>
<span data-ttu-id="54c33-109">Polecenie cmdlet **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** synchronizuje poświadczenia lokalne między węzłami środowiska wykonawczego programu integracyjnego, które wymuszają identyczne poświadczenia we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="54c33-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="54c33-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54c33-110">EXAMPLES</span></span>

### <span data-ttu-id="54c33-111">Przykład 1: synchronizowanie poświadczenia środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="54c33-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="54c33-112">Polecenie cmdlet synchronizuje poświadczenia między węzłami środowiska wykonawczego programu integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="54c33-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="54c33-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54c33-113">PARAMETERS</span></span>

### <span data-ttu-id="54c33-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54c33-114">-Confirm</span></span>
<span data-ttu-id="54c33-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c33-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c33-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="54c33-116">-DataFactoryName</span></span>
<span data-ttu-id="54c33-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="54c33-117">The data factory name.</span></span>

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

### <span data-ttu-id="54c33-118">-Force</span><span class="sxs-lookup"><span data-stu-id="54c33-118">-Force</span></span>
<span data-ttu-id="54c33-119">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="54c33-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c33-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54c33-120">-InputObject</span></span>
<span data-ttu-id="54c33-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="54c33-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="54c33-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="54c33-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="54c33-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="54c33-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c33-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c33-124">-ResourceGroupName</span></span>
<span data-ttu-id="54c33-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54c33-125">The resource group name.</span></span>

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

### <span data-ttu-id="54c33-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c33-126">-ResourceId</span></span>
<span data-ttu-id="54c33-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="54c33-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="54c33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c33-128">-WhatIf</span></span>
<span data-ttu-id="54c33-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c33-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="54c33-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54c33-130">INPUTS</span></span>

### <span data-ttu-id="54c33-131">System. String</span><span class="sxs-lookup"><span data-stu-id="54c33-131">System.String</span></span>
<span data-ttu-id="54c33-132">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="54c33-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="54c33-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54c33-133">OUTPUTS</span></span>

### <span data-ttu-id="54c33-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="54c33-134">System.Object</span></span>

## <span data-ttu-id="54c33-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54c33-135">NOTES</span></span>

## <span data-ttu-id="54c33-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54c33-136">RELATED LINKS</span></span>
