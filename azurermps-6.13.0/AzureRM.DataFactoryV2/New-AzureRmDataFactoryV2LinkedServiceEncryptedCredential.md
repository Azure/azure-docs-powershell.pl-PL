---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 765bd2c75a377204ab4566f47d0498deaf127953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524497"
---
# <span data-ttu-id="690ec-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="690ec-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="690ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="690ec-102">SYNOPSIS</span></span>
<span data-ttu-id="690ec-103">Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="690ec-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="690ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="690ec-104">SYNTAX</span></span>

### <span data-ttu-id="690ec-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="690ec-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690ec-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="690ec-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690ec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="690ec-107">DESCRIPTION</span></span>
<span data-ttu-id="690ec-108">Polecenie cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="690ec-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="690ec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="690ec-109">EXAMPLES</span></span>

### <span data-ttu-id="690ec-110">Przykład 1: szyfrowanie creadentials w połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="690ec-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="690ec-111">To polecenie szyfruje poświadczenia w pliku D:\sql.jsprzy użyciu środowiska wykonawczego integracji o nazwie myIR.</span><span class="sxs-lookup"><span data-stu-id="690ec-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="690ec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="690ec-112">PARAMETERS</span></span>

### <span data-ttu-id="690ec-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="690ec-113">-DataFactory</span></span>
<span data-ttu-id="690ec-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="690ec-114">The data factory object.</span></span>

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

### <span data-ttu-id="690ec-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="690ec-115">-DataFactoryName</span></span>
<span data-ttu-id="690ec-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="690ec-116">The data factory name.</span></span>

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

### <span data-ttu-id="690ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690ec-117">-DefaultProfile</span></span>
<span data-ttu-id="690ec-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="690ec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="690ec-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="690ec-119">-DefinitionFile</span></span>
<span data-ttu-id="690ec-120">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="690ec-120">The JSON file path.</span></span>

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

### <span data-ttu-id="690ec-121">-Force</span><span class="sxs-lookup"><span data-stu-id="690ec-121">-Force</span></span>
<span data-ttu-id="690ec-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="690ec-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="690ec-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="690ec-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="690ec-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="690ec-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="690ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="690ec-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="690ec-126">The resource group name.</span></span>

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

### <span data-ttu-id="690ec-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="690ec-127">-Confirm</span></span>
<span data-ttu-id="690ec-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="690ec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="690ec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690ec-129">-WhatIf</span></span>
<span data-ttu-id="690ec-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="690ec-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="690ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690ec-131">CommonParameters</span></span>
<span data-ttu-id="690ec-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690ec-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690ec-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690ec-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="690ec-134">INPUTS</span></span>

### <span data-ttu-id="690ec-135">System. String</span><span class="sxs-lookup"><span data-stu-id="690ec-135">System.String</span></span>

### <span data-ttu-id="690ec-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="690ec-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="690ec-137">Parametry: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="690ec-137">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="690ec-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="690ec-138">OUTPUTS</span></span>

### <span data-ttu-id="690ec-139">System. String</span><span class="sxs-lookup"><span data-stu-id="690ec-139">System.String</span></span>

## <span data-ttu-id="690ec-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="690ec-140">NOTES</span></span>

## <span data-ttu-id="690ec-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="690ec-141">RELATED LINKS</span></span>
