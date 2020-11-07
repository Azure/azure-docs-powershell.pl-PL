---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718542"
---
# <span data-ttu-id="05e2f-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="05e2f-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="05e2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="05e2f-103">Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="05e2f-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05e2f-104">SYNTAX</span></span>

### <span data-ttu-id="05e2f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05e2f-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="05e2f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="05e2f-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="05e2f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="05e2f-108">Polecenie cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="05e2f-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="05e2f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05e2f-109">EXAMPLES</span></span>

### <span data-ttu-id="05e2f-110">Przykład 1: szyfrowanie creadentials w połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="05e2f-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="05e2f-111">To polecenie szyfruje poświadczenia w pliku D:\sql.jsprzy użyciu środowiska wykonawczego integracji o nazwie myIR.</span><span class="sxs-lookup"><span data-stu-id="05e2f-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="05e2f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05e2f-112">PARAMETERS</span></span>

### <span data-ttu-id="05e2f-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="05e2f-113">-DataFactory</span></span>
<span data-ttu-id="05e2f-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="05e2f-114">The data factory object.</span></span>

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

### <span data-ttu-id="05e2f-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="05e2f-115">-DataFactoryName</span></span>
<span data-ttu-id="05e2f-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="05e2f-116">The data factory name.</span></span>

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

### <span data-ttu-id="05e2f-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="05e2f-117">-DefinitionFile</span></span>
<span data-ttu-id="05e2f-118">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="05e2f-118">The JSON file path.</span></span>

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

### <span data-ttu-id="05e2f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="05e2f-119">-Force</span></span>
<span data-ttu-id="05e2f-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="05e2f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="05e2f-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="05e2f-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="05e2f-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="05e2f-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="05e2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="05e2f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05e2f-124">The resource group name.</span></span>

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

### <span data-ttu-id="05e2f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05e2f-125">-Confirm</span></span>
<span data-ttu-id="05e2f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e2f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05e2f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e2f-127">-WhatIf</span></span>
<span data-ttu-id="05e2f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e2f-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="05e2f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05e2f-129">INPUTS</span></span>

### <span data-ttu-id="05e2f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="05e2f-130">System.String</span></span>
<span data-ttu-id="05e2f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="05e2f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="05e2f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05e2f-132">OUTPUTS</span></span>

### <span data-ttu-id="05e2f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="05e2f-133">System.String</span></span>


## <span data-ttu-id="05e2f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05e2f-134">NOTES</span></span>

## <span data-ttu-id="05e2f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05e2f-135">RELATED LINKS</span></span>

