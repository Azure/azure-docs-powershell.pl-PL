---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 11d87742e34ae387f765551f93add5a1c300421a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971185"
---
# <span data-ttu-id="cf3dc-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cf3dc-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="cf3dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf3dc-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3dc-103">Generuj samodzielnie hostowany klucz środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="cf3dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf3dc-104">SYNTAX</span></span>

### <span data-ttu-id="cf3dc-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cf3dc-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3dc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf3dc-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3dc-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cf3dc-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf3dc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf3dc-108">DESCRIPTION</span></span>
<span data-ttu-id="cf3dc-109">Polecenie cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** ponownie generuje klucz środowiska uruchomieniowego integracji z nazwą klucza określoną przez parametr "KeyName".</span><span class="sxs-lookup"><span data-stu-id="cf3dc-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="cf3dc-110">Poprzedni klucz jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="cf3dc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf3dc-111">EXAMPLES</span></span>

### <span data-ttu-id="cf3dc-112">Przykład 1. Generowanie nowego klucza dla środowiska uruchomieniowego integracji</span><span class="sxs-lookup"><span data-stu-id="cf3dc-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="cf3dc-113">Polecenie cmdlet ponownie generuje klucz "authKey2" dla środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="cf3dc-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cf3dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf3dc-114">PARAMETERS</span></span>

### <span data-ttu-id="cf3dc-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf3dc-115">-DataFactoryName</span></span>
<span data-ttu-id="cf3dc-116">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-116">The data factory name.</span></span>

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

### <span data-ttu-id="cf3dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3dc-117">-DefaultProfile</span></span>
<span data-ttu-id="cf3dc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf3dc-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cf3dc-119">-Force</span></span>
<span data-ttu-id="cf3dc-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cf3dc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf3dc-121">-InputObject</span></span>
<span data-ttu-id="cf3dc-122">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="cf3dc-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cf3dc-123">-KeyName</span></span>
<span data-ttu-id="cf3dc-124">Nazwa klucza uwierzytelniania środowiska integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="cf3dc-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf3dc-125">-Name</span></span>
<span data-ttu-id="cf3dc-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="cf3dc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3dc-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf3dc-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-128">The resource group name.</span></span>

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

### <span data-ttu-id="cf3dc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf3dc-129">-ResourceId</span></span>
<span data-ttu-id="cf3dc-130">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cf3dc-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf3dc-131">-Confirm</span></span>
<span data-ttu-id="cf3dc-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf3dc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf3dc-133">-WhatIf</span></span>
<span data-ttu-id="cf3dc-134">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cf3dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3dc-135">CommonParameters</span></span>
<span data-ttu-id="cf3dc-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3dc-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf3dc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3dc-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf3dc-138">INPUTS</span></span>

### <span data-ttu-id="cf3dc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cf3dc-139">System.String</span></span>

### <span data-ttu-id="cf3dc-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf3dc-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cf3dc-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf3dc-141">OUTPUTS</span></span>

### <span data-ttu-id="cf3dc-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="cf3dc-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="cf3dc-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf3dc-143">NOTES</span></span>

## <span data-ttu-id="cf3dc-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf3dc-144">RELATED LINKS</span></span>

[<span data-ttu-id="cf3dc-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cf3dc-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
