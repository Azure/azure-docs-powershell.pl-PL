---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 0ff9ef1337a1f2a5f0503c59dc4e6240d3c959b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062350"
---
# <span data-ttu-id="0a9d0-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="0a9d0-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="0a9d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9d0-103">Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="0a9d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a9d0-104">SYNTAX</span></span>

### <span data-ttu-id="0a9d0-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a9d0-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a9d0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0a9d0-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a9d0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0a9d0-107">DESCRIPTION</span></span>
<span data-ttu-id="0a9d0-108">Polecenie cmdlet New-AzDataFactoryV2LinkedServiceEncryptedCredential Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="0a9d0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a9d0-109">EXAMPLES</span></span>

### <span data-ttu-id="0a9d0-110">Przykład 1: szyfrowanie poświadczeń w połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="0a9d0-110">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="0a9d0-111">To polecenie szyfruje poświadczenia w pliku C:\samples\WikiSample\TaxiDemo1.jsprzy użyciu środowiska wykonawczego Integration o nazwie test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-111">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="0a9d0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a9d0-112">PARAMETERS</span></span>

### <span data-ttu-id="0a9d0-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a9d0-113">-DataFactory</span></span>
<span data-ttu-id="0a9d0-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-114">The data factory object.</span></span>

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

### <span data-ttu-id="0a9d0-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0a9d0-115">-DataFactoryName</span></span>
<span data-ttu-id="0a9d0-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-116">The data factory name.</span></span>

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

### <span data-ttu-id="0a9d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9d0-117">-DefaultProfile</span></span>
<span data-ttu-id="0a9d0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a9d0-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0a9d0-119">-DefinitionFile</span></span>
<span data-ttu-id="0a9d0-120">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-120">The JSON file path.</span></span>

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

### <span data-ttu-id="0a9d0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0a9d0-121">-Force</span></span>
<span data-ttu-id="0a9d0-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0a9d0-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="0a9d0-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0a9d0-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="0a9d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a9d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a9d0-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-126">The resource group name.</span></span>

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

### <span data-ttu-id="0a9d0-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a9d0-127">-Confirm</span></span>
<span data-ttu-id="0a9d0-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a9d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a9d0-129">-WhatIf</span></span>
<span data-ttu-id="0a9d0-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0a9d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9d0-131">CommonParameters</span></span>
<span data-ttu-id="0a9d0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a9d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9d0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a9d0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9d0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a9d0-134">INPUTS</span></span>

### <span data-ttu-id="0a9d0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0a9d0-135">System.String</span></span>

### <span data-ttu-id="0a9d0-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0a9d0-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0a9d0-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a9d0-137">OUTPUTS</span></span>

### <span data-ttu-id="0a9d0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0a9d0-138">System.String</span></span>

## <span data-ttu-id="0a9d0-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a9d0-139">NOTES</span></span>

## <span data-ttu-id="0a9d0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a9d0-140">RELATED LINKS</span></span>
