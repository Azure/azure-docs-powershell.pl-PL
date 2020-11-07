---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: becbcd3e7bbc0a86a2b092921fd5060dd56e927b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719347"
---
# <span data-ttu-id="0e462-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0e462-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="0e462-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e462-102">SYNOPSIS</span></span>
<span data-ttu-id="0e462-103">Ponowne generowanie klucza środowiska uruchomieniowego w ramach samodzielnej integracji.</span><span class="sxs-lookup"><span data-stu-id="0e462-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e462-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e462-104">SYNTAX</span></span>

### <span data-ttu-id="0e462-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e462-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e462-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e462-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e462-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0e462-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e462-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0e462-108">DESCRIPTION</span></span>
<span data-ttu-id="0e462-109">Polecenie cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** generuje ponownie klucz środowiska uruchomieniowego integracji z nazwą klucza określoną przez parametr "KeyName".</span><span class="sxs-lookup"><span data-stu-id="0e462-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="0e462-110">Poprzedni klucz będzie nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="0e462-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="0e462-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e462-111">EXAMPLES</span></span>

### <span data-ttu-id="0e462-112">Przykład 1. Generuj nowy klucz dla środowiska wykonawczego integracji</span><span class="sxs-lookup"><span data-stu-id="0e462-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="0e462-113">Polecenie cmdlet regeneruje klucz "authKey2" dla środowiska uruchomieniowego integracji o nazwie "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="0e462-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0e462-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e462-114">PARAMETERS</span></span>

### <span data-ttu-id="0e462-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e462-115">-Confirm</span></span>
<span data-ttu-id="0e462-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e462-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e462-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0e462-117">-DataFactoryName</span></span>
<span data-ttu-id="0e462-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0e462-118">The data factory name.</span></span>

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

### <span data-ttu-id="0e462-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0e462-119">-Force</span></span>
<span data-ttu-id="0e462-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e462-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0e462-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e462-121">-InputObject</span></span>
<span data-ttu-id="0e462-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="0e462-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="0e462-123">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="0e462-123">-KeyName</span></span>
<span data-ttu-id="0e462-124">Nazwa klucza uwierzytelniania w ramach samodzielnego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="0e462-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e462-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e462-125">-Name</span></span>
<span data-ttu-id="0e462-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="0e462-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="0e462-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e462-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e462-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e462-128">The resource group name.</span></span>

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

### <span data-ttu-id="0e462-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e462-129">-ResourceId</span></span>
<span data-ttu-id="0e462-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e462-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0e462-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e462-131">-WhatIf</span></span>
<span data-ttu-id="0e462-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e462-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0e462-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e462-133">-DefaultProfile</span></span>
<span data-ttu-id="0e462-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e462-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e462-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e462-135">CommonParameters</span></span>
<span data-ttu-id="0e462-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e462-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e462-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e462-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e462-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e462-138">INPUTS</span></span>

### <span data-ttu-id="0e462-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0e462-139">System.String</span></span>
<span data-ttu-id="0e462-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0e462-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0e462-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e462-141">OUTPUTS</span></span>

### <span data-ttu-id="0e462-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="0e462-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="0e462-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e462-143">NOTES</span></span>

## <span data-ttu-id="0e462-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e462-144">RELATED LINKS</span></span>

[<span data-ttu-id="0e462-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0e462-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
