---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 47121a8a06e2b4aa4e48218d1be4694743c00de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525185"
---
# <span data-ttu-id="3b44a-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="3b44a-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="3b44a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b44a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b44a-103">Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="3b44a-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b44a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b44a-104">SYNTAX</span></span>

### <span data-ttu-id="3b44a-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b44a-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b44a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3b44a-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b44a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3b44a-107">DESCRIPTION</span></span>
<span data-ttu-id="3b44a-108">Polecenie cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="3b44a-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="3b44a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b44a-109">EXAMPLES</span></span>

### <span data-ttu-id="3b44a-110">Przykład 1: szyfrowanie creadentials w połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="3b44a-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="3b44a-111">To polecenie szyfruje poświadczenia w pliku D:\sql.jsprzy użyciu środowiska wykonawczego integracji o nazwie myIR.</span><span class="sxs-lookup"><span data-stu-id="3b44a-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="3b44a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b44a-112">PARAMETERS</span></span>

### <span data-ttu-id="3b44a-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3b44a-113">-DataFactory</span></span>
<span data-ttu-id="3b44a-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3b44a-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b44a-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3b44a-115">-DataFactoryName</span></span>
<span data-ttu-id="3b44a-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3b44a-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b44a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b44a-117">-DefaultProfile</span></span>
<span data-ttu-id="3b44a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b44a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b44a-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3b44a-119">-DefinitionFile</span></span>
<span data-ttu-id="3b44a-120">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="3b44a-120">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b44a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3b44a-121">-Force</span></span>
<span data-ttu-id="3b44a-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b44a-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3b44a-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3b44a-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="3b44a-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="3b44a-124">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b44a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b44a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3b44a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b44a-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b44a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b44a-127">-Confirm</span></span>
<span data-ttu-id="3b44a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b44a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b44a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b44a-129">-WhatIf</span></span>
<span data-ttu-id="3b44a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b44a-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3b44a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b44a-131">CommonParameters</span></span>
<span data-ttu-id="3b44a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b44a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b44a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b44a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b44a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b44a-134">INPUTS</span></span>

### <span data-ttu-id="3b44a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3b44a-135">System.String</span></span>
<span data-ttu-id="3b44a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3b44a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3b44a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b44a-137">OUTPUTS</span></span>

### <span data-ttu-id="3b44a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3b44a-138">System.String</span></span>

## <span data-ttu-id="3b44a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b44a-139">NOTES</span></span>

## <span data-ttu-id="3b44a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b44a-140">RELATED LINKS</span></span>

