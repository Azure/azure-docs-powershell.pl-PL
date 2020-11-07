---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2ac4868905ee1de93f87ecb17d6b9ced0f036cda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525186"
---
# <span data-ttu-id="2b784-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2b784-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="2b784-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b784-102">SYNOPSIS</span></span>
<span data-ttu-id="2b784-103">Ponowne generowanie klucza środowiska uruchomieniowego w ramach samodzielnej integracji.</span><span class="sxs-lookup"><span data-stu-id="2b784-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b784-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b784-104">SYNTAX</span></span>

### <span data-ttu-id="2b784-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2b784-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b784-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b784-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b784-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2b784-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b784-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2b784-108">DESCRIPTION</span></span>
<span data-ttu-id="2b784-109">Polecenie cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** generuje ponownie klucz środowiska uruchomieniowego integracji z nazwą klucza określoną przez parametr "KeyName".</span><span class="sxs-lookup"><span data-stu-id="2b784-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="2b784-110">Poprzedni klucz będzie nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="2b784-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="2b784-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b784-111">EXAMPLES</span></span>

### <span data-ttu-id="2b784-112">Przykład 1. Generuj nowy klucz dla środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="2b784-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="2b784-113">Polecenie cmdlet regeneruje klucz "authKey2" dla środowiska uruchomieniowego integracji o nazwie "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="2b784-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2b784-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b784-114">PARAMETERS</span></span>

### <span data-ttu-id="2b784-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2b784-115">-DataFactoryName</span></span>
<span data-ttu-id="2b784-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="2b784-116">The data factory name.</span></span>

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

### <span data-ttu-id="2b784-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b784-117">-DefaultProfile</span></span>
<span data-ttu-id="2b784-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b784-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b784-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2b784-119">-Force</span></span>
<span data-ttu-id="2b784-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2b784-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2b784-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2b784-121">-InputObject</span></span>
<span data-ttu-id="2b784-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="2b784-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="2b784-123">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="2b784-123">-KeyName</span></span>
<span data-ttu-id="2b784-124">Nazwa klucza uwierzytelniania w ramach samodzielnego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="2b784-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b784-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b784-125">-Name</span></span>
<span data-ttu-id="2b784-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="2b784-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="2b784-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b784-127">-ResourceGroupName</span></span>
<span data-ttu-id="2b784-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b784-128">The resource group name.</span></span>

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

### <span data-ttu-id="2b784-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b784-129">-ResourceId</span></span>
<span data-ttu-id="2b784-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2b784-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2b784-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b784-131">-Confirm</span></span>
<span data-ttu-id="2b784-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b784-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b784-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b784-133">-WhatIf</span></span>
<span data-ttu-id="2b784-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b784-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2b784-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b784-135">CommonParameters</span></span>
<span data-ttu-id="2b784-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b784-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b784-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b784-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b784-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b784-138">INPUTS</span></span>

### <span data-ttu-id="2b784-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2b784-139">System.String</span></span>
<span data-ttu-id="2b784-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2b784-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2b784-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b784-141">OUTPUTS</span></span>

### <span data-ttu-id="2b784-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="2b784-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="2b784-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b784-143">NOTES</span></span>

## <span data-ttu-id="2b784-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b784-144">RELATED LINKS</span></span>

[<span data-ttu-id="2b784-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="2b784-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()