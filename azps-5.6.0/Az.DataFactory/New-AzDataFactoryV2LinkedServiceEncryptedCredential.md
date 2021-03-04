---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 678cc7e015321d90fee5a5340caeeeb861b30600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971162"
---
# <span data-ttu-id="d8af3-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="d8af3-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="d8af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8af3-102">SYNOPSIS</span></span>
<span data-ttu-id="d8af3-103">Szyfrowanie poświadczeń w połączonej usłudze w określonym środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="d8af3-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="d8af3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8af3-104">SYNTAX</span></span>

### <span data-ttu-id="d8af3-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="d8af3-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8af3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d8af3-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8af3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8af3-107">DESCRIPTION</span></span>
<span data-ttu-id="d8af3-108">Polecenie New-AzDataFactoryV2LinkedServiceEncryptedCredential szyfrowania poświadczeń w połączonej usłudze w określonym środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="d8af3-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="d8af3-109">Upewnij się, że są spełnione następujące wymagania wstępne:</span><span class="sxs-lookup"><span data-stu-id="d8af3-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="d8af3-110">**Opcja dostępu zdalnego** jest włączona w środowisku integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="d8af3-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="d8af3-111">Do wykonywania polecenia cmdlet jest używany program PowerShell 7.0 lub wyższy.</span><span class="sxs-lookup"><span data-stu-id="d8af3-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="d8af3-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8af3-112">EXAMPLES</span></span>

### <span data-ttu-id="d8af3-113">Przykład 1. Szyfrowanie poświadczeń w połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="d8af3-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="d8af3-114">To polecenie szyfruje poświadczenia w pliku i C:\samples\WikiSample\TaxiDemo1.jsw środowisku uruchomieniowym integracji o nazwie test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="d8af3-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="d8af3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8af3-115">PARAMETERS</span></span>

### <span data-ttu-id="d8af3-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8af3-116">-DataFactory</span></span>
<span data-ttu-id="d8af3-117">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="d8af3-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8af3-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8af3-118">-DataFactoryName</span></span>
<span data-ttu-id="d8af3-119">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="d8af3-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8af3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8af3-120">-DefaultProfile</span></span>
<span data-ttu-id="d8af3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8af3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8af3-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d8af3-122">-DefinitionFile</span></span>
<span data-ttu-id="d8af3-123">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="d8af3-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8af3-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d8af3-124">-Force</span></span>
<span data-ttu-id="d8af3-125">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8af3-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d8af3-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d8af3-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d8af3-127">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="d8af3-127">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8af3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8af3-128">-ResourceGroupName</span></span>
<span data-ttu-id="d8af3-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8af3-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8af3-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8af3-130">-Confirm</span></span>
<span data-ttu-id="d8af3-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8af3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8af3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8af3-132">-WhatIf</span></span>
<span data-ttu-id="d8af3-133">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8af3-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d8af3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8af3-134">CommonParameters</span></span>
<span data-ttu-id="d8af3-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8af3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8af3-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8af3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8af3-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8af3-137">INPUTS</span></span>

### <span data-ttu-id="d8af3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d8af3-138">System.String</span></span>

### <span data-ttu-id="d8af3-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d8af3-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d8af3-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8af3-140">OUTPUTS</span></span>

### <span data-ttu-id="d8af3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d8af3-141">System.String</span></span>

## <span data-ttu-id="d8af3-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8af3-142">NOTES</span></span>

## <span data-ttu-id="d8af3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8af3-143">RELATED LINKS</span></span>
