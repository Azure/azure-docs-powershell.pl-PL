---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: cca0b397f85a0e0fd42f1e3331294881e1e89014
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716495"
---
# <span data-ttu-id="84b02-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="84b02-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="84b02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84b02-102">SYNOPSIS</span></span>
<span data-ttu-id="84b02-103">Pobiera informacje o koncentratorach w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="84b02-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84b02-104">SYNTAX</span></span>

### <span data-ttu-id="84b02-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84b02-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84b02-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="84b02-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84b02-107">Opis</span><span class="sxs-lookup"><span data-stu-id="84b02-107">DESCRIPTION</span></span>
<span data-ttu-id="84b02-108">Polecenie cmdlet **Get-AzureRmDataFactoryHub** pobiera informacje o koncentratorach w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="84b02-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="84b02-109">Jeśli określisz nazwę koncentratora, to polecenie cmdlet będzie pobierać informacje o tym koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="84b02-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="84b02-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich koncentratorach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="84b02-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="84b02-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84b02-111">EXAMPLES</span></span>

### <span data-ttu-id="84b02-112">Przykład 1: pobieranie wszystkich koncentratorów danych</span><span class="sxs-lookup"><span data-stu-id="84b02-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="84b02-113">To polecenie pobiera wszystkie centra danych w grupie zasobów platformy Azure o nazwie ADFResourceGroup oraz fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="84b02-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="84b02-114">Przykład 2: uzyskiwanie określonego centrum danych</span><span class="sxs-lookup"><span data-stu-id="84b02-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="84b02-115">To polecenie pobiera informacje o centrum o nazwie MyDataHub w grupie zasobów platformy Azure o nazwie ADFResourceGroup i fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="84b02-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="84b02-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84b02-116">PARAMETERS</span></span>

### <span data-ttu-id="84b02-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="84b02-117">-DataFactory</span></span>
<span data-ttu-id="84b02-118">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="84b02-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="84b02-119">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach w fabryce danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="84b02-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b02-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="84b02-120">-DataFactoryName</span></span>
<span data-ttu-id="84b02-121">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="84b02-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="84b02-122">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach w fabryce danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="84b02-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="84b02-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b02-123">-DefaultProfile</span></span>
<span data-ttu-id="84b02-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="84b02-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84b02-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84b02-125">-Name</span></span>
<span data-ttu-id="84b02-126">Określa nazwę centrum, o którym należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="84b02-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b02-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b02-127">-ResourceGroupName</span></span>
<span data-ttu-id="84b02-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="84b02-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="84b02-129">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="84b02-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="84b02-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b02-130">CommonParameters</span></span>
<span data-ttu-id="84b02-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b02-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b02-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b02-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b02-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84b02-133">INPUTS</span></span>

### <span data-ttu-id="84b02-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="84b02-134">None</span></span>
<span data-ttu-id="84b02-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="84b02-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84b02-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84b02-136">OUTPUTS</span></span>

### <span data-ttu-id="84b02-137">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. datafactors. MODELES. PSHub]</span><span class="sxs-lookup"><span data-stu-id="84b02-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="84b02-138">Microsoft. Azure. Commands. datafactors. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="84b02-138">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="84b02-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84b02-139">NOTES</span></span>
* <span data-ttu-id="84b02-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="84b02-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="84b02-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84b02-141">RELATED LINKS</span></span>

[<span data-ttu-id="84b02-142">Nowe — AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="84b02-142">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="84b02-143">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="84b02-143">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


