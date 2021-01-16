---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344638"
---
# <span data-ttu-id="f0602-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="f0602-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="f0602-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0602-102">SYNOPSIS</span></span>
<span data-ttu-id="f0602-103">Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="f0602-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="f0602-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0602-104">SYNTAX</span></span>

### <span data-ttu-id="f0602-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f0602-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0602-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f0602-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0602-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f0602-107">DESCRIPTION</span></span>
<span data-ttu-id="f0602-108">Polecenie cmdlet New-AzDataFactoryV2LinkedServiceEncryptedCredential Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="f0602-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="f0602-109">Upewnij się, że zostały spełnione następujące wymagania wstępne:</span><span class="sxs-lookup"><span data-stu-id="f0602-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="f0602-110">Opcja **dostęp zdalny** jest włączona w środowisku wykonawczym integracji samodzielnej.</span><span class="sxs-lookup"><span data-stu-id="f0602-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="f0602-111">Do wykonania polecenia cmdlet jest wykorzystywany program PowerShell w wersji 7,0 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="f0602-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="f0602-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0602-112">EXAMPLES</span></span>

### <span data-ttu-id="f0602-113">Przykład 1: szyfrowanie poświadczeń w połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="f0602-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="f0602-114">To polecenie szyfruje poświadczenia w pliku C:\samples\WikiSample\TaxiDemo1.jsprzy użyciu środowiska wykonawczego Integration o nazwie test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="f0602-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="f0602-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0602-115">PARAMETERS</span></span>

### <span data-ttu-id="f0602-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f0602-116">-DataFactory</span></span>
<span data-ttu-id="f0602-117">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f0602-117">The data factory object.</span></span>

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

### <span data-ttu-id="f0602-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f0602-118">-DataFactoryName</span></span>
<span data-ttu-id="f0602-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f0602-119">The data factory name.</span></span>

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

### <span data-ttu-id="f0602-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0602-120">-DefaultProfile</span></span>
<span data-ttu-id="f0602-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0602-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0602-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f0602-122">-DefinitionFile</span></span>
<span data-ttu-id="f0602-123">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="f0602-123">The JSON file path.</span></span>

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

### <span data-ttu-id="f0602-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f0602-124">-Force</span></span>
<span data-ttu-id="f0602-125">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0602-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f0602-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f0602-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f0602-127">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="f0602-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="f0602-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0602-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0602-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0602-129">The resource group name.</span></span>

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

### <span data-ttu-id="f0602-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0602-130">-Confirm</span></span>
<span data-ttu-id="f0602-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0602-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0602-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0602-132">-WhatIf</span></span>
<span data-ttu-id="f0602-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0602-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f0602-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0602-134">CommonParameters</span></span>
<span data-ttu-id="f0602-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0602-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0602-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0602-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0602-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0602-137">INPUTS</span></span>

### <span data-ttu-id="f0602-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f0602-138">System.String</span></span>

### <span data-ttu-id="f0602-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f0602-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f0602-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0602-140">OUTPUTS</span></span>

### <span data-ttu-id="f0602-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f0602-141">System.String</span></span>

## <span data-ttu-id="f0602-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0602-142">NOTES</span></span>

## <span data-ttu-id="f0602-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0602-143">RELATED LINKS</span></span>
