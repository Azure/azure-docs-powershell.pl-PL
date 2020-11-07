---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 40f6a6c5f446b23a92a2ca5c5c8c872297b2a81a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868659"
---
# <span data-ttu-id="00676-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="00676-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="00676-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00676-102">SYNOPSIS</span></span>
<span data-ttu-id="00676-103">Synchronizuje poświadczenia między węzłami w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="00676-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="00676-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00676-104">SYNTAX</span></span>

### <span data-ttu-id="00676-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="00676-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00676-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00676-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00676-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="00676-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00676-108">Opis</span><span class="sxs-lookup"><span data-stu-id="00676-108">DESCRIPTION</span></span>
<span data-ttu-id="00676-109">Polecenie cmdlet **Sync-AzDataFactoryV2IntegrationRuntimeCredential** synchronizuje poświadczenia lokalne między węzłami środowiska wykonawczego programu integracyjnego, które wymuszają identyczne poświadczenia we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="00676-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="00676-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00676-110">EXAMPLES</span></span>

### <span data-ttu-id="00676-111">Przykład 1: synchronizowanie poświadczenia środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="00676-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="00676-112">Polecenie cmdlet synchronizuje poświadczenia między węzłami środowiska wykonawczego programu integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="00676-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="00676-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00676-113">PARAMETERS</span></span>

### <span data-ttu-id="00676-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="00676-114">-DataFactoryName</span></span>
<span data-ttu-id="00676-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="00676-115">The data factory name.</span></span>

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

### <span data-ttu-id="00676-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00676-116">-DefaultProfile</span></span>
<span data-ttu-id="00676-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00676-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00676-118">-Force</span><span class="sxs-lookup"><span data-stu-id="00676-118">-Force</span></span>
<span data-ttu-id="00676-119">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00676-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="00676-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="00676-120">-InputObject</span></span>
<span data-ttu-id="00676-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="00676-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="00676-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="00676-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="00676-123">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="00676-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="00676-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00676-124">-ResourceGroupName</span></span>
<span data-ttu-id="00676-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="00676-125">The resource group name.</span></span>

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

### <span data-ttu-id="00676-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00676-126">-ResourceId</span></span>
<span data-ttu-id="00676-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00676-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="00676-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00676-128">-Confirm</span></span>
<span data-ttu-id="00676-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00676-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00676-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00676-130">-WhatIf</span></span>
<span data-ttu-id="00676-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00676-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="00676-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00676-132">CommonParameters</span></span>
<span data-ttu-id="00676-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00676-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00676-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00676-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00676-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00676-135">INPUTS</span></span>

### <span data-ttu-id="00676-136">System. String</span><span class="sxs-lookup"><span data-stu-id="00676-136">System.String</span></span>

### <span data-ttu-id="00676-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="00676-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="00676-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00676-138">OUTPUTS</span></span>

### <span data-ttu-id="00676-139">System. void</span><span class="sxs-lookup"><span data-stu-id="00676-139">System.Void</span></span>

## <span data-ttu-id="00676-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00676-140">NOTES</span></span>

## <span data-ttu-id="00676-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00676-141">RELATED LINKS</span></span>
