---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: bdc3d9b997a98ca67c2848ada32d8fc94fa20e09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705984"
---
# <span data-ttu-id="34dd4-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="34dd4-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="34dd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="34dd4-103">Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="34dd4-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="34dd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34dd4-104">SYNTAX</span></span>

### <span data-ttu-id="34dd4-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34dd4-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34dd4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="34dd4-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34dd4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34dd4-107">DESCRIPTION</span></span>
<span data-ttu-id="34dd4-108">Polecenie cmdlet New-AzDataFactoryV2LinkedServiceEncryptCredential Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="34dd4-108">The New-AzDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="34dd4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34dd4-109">EXAMPLES</span></span>

### <span data-ttu-id="34dd4-110">Przykład 1: szyfrowanie poświadczeń w połączonej usłudze</span><span class="sxs-lookup"><span data-stu-id="34dd4-110">Example 1: Encrypt credentials in a linked service</span></span>
```
PS C:\> New-AzDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="34dd4-111">To polecenie szyfruje poświadczenia w pliku D:\sql.jsprzy użyciu środowiska wykonawczego integracji o nazwie myIR.</span><span class="sxs-lookup"><span data-stu-id="34dd4-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="34dd4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34dd4-112">PARAMETERS</span></span>

### <span data-ttu-id="34dd4-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="34dd4-113">-DataFactory</span></span>
<span data-ttu-id="34dd4-114">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="34dd4-114">The data factory object.</span></span>

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

### <span data-ttu-id="34dd4-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="34dd4-115">-DataFactoryName</span></span>
<span data-ttu-id="34dd4-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="34dd4-116">The data factory name.</span></span>

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

### <span data-ttu-id="34dd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34dd4-117">-DefaultProfile</span></span>
<span data-ttu-id="34dd4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34dd4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34dd4-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="34dd4-119">-DefinitionFile</span></span>
<span data-ttu-id="34dd4-120">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="34dd4-120">The JSON file path.</span></span>

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

### <span data-ttu-id="34dd4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="34dd4-121">-Force</span></span>
<span data-ttu-id="34dd4-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34dd4-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="34dd4-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="34dd4-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="34dd4-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="34dd4-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="34dd4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34dd4-125">-ResourceGroupName</span></span>
<span data-ttu-id="34dd4-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34dd4-126">The resource group name.</span></span>

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

### <span data-ttu-id="34dd4-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34dd4-127">-Confirm</span></span>
<span data-ttu-id="34dd4-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34dd4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34dd4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34dd4-129">-WhatIf</span></span>
<span data-ttu-id="34dd4-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34dd4-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="34dd4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34dd4-131">CommonParameters</span></span>
<span data-ttu-id="34dd4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34dd4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34dd4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34dd4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34dd4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34dd4-134">INPUTS</span></span>

### <span data-ttu-id="34dd4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="34dd4-135">System.String</span></span>

### <span data-ttu-id="34dd4-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="34dd4-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="34dd4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34dd4-137">OUTPUTS</span></span>

### <span data-ttu-id="34dd4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="34dd4-138">System.String</span></span>

## <span data-ttu-id="34dd4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34dd4-139">NOTES</span></span>

## <span data-ttu-id="34dd4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34dd4-140">RELATED LINKS</span></span>
