---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: a96d8d3d9025e473b5c08d84201fde2a10d8be34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553955"
---
# <span data-ttu-id="11ce7-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="11ce7-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="11ce7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="11ce7-103">Pobiera informacje o koncentratorach w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="11ce7-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11ce7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11ce7-104">SYNTAX</span></span>

### <span data-ttu-id="11ce7-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11ce7-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11ce7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="11ce7-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11ce7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="11ce7-107">DESCRIPTION</span></span>
<span data-ttu-id="11ce7-108">Polecenie cmdlet **Get-AzureRmDataFactoryHub** pobiera informacje o koncentratorach w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="11ce7-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="11ce7-109">Jeśli określisz nazwę koncentratora, to polecenie cmdlet będzie pobierać informacje o tym koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="11ce7-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="11ce7-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich koncentratorach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="11ce7-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="11ce7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11ce7-111">EXAMPLES</span></span>

### <span data-ttu-id="11ce7-112">Przykład 1: pobieranie wszystkich koncentratorów danych</span><span class="sxs-lookup"><span data-stu-id="11ce7-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="11ce7-113">To polecenie pobiera wszystkie centra danych w grupie zasobów platformy Azure o nazwie ADFResourceGroup oraz fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="11ce7-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="11ce7-114">Przykład 2: uzyskiwanie określonego centrum danych</span><span class="sxs-lookup"><span data-stu-id="11ce7-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="11ce7-115">To polecenie pobiera informacje o centrum o nazwie MyDataHub w grupie zasobów platformy Azure o nazwie ADFResourceGroup i fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="11ce7-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="11ce7-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11ce7-116">PARAMETERS</span></span>

### <span data-ttu-id="11ce7-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="11ce7-117">-DataFactory</span></span>
<span data-ttu-id="11ce7-118">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="11ce7-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="11ce7-119">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach w fabryce danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="11ce7-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ce7-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="11ce7-120">-DataFactoryName</span></span>
<span data-ttu-id="11ce7-121">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="11ce7-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="11ce7-122">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach w fabryce danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="11ce7-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="11ce7-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11ce7-123">-Name</span></span>
<span data-ttu-id="11ce7-124">Określa nazwę centrum, o którym należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="11ce7-124">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ce7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ce7-125">-ResourceGroupName</span></span>
<span data-ttu-id="11ce7-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11ce7-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="11ce7-127">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="11ce7-127">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="11ce7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ce7-128">-DefaultProfile</span></span>
<span data-ttu-id="11ce7-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11ce7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11ce7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ce7-130">CommonParameters</span></span>
<span data-ttu-id="11ce7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ce7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ce7-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ce7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ce7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11ce7-133">INPUTS</span></span>

## <span data-ttu-id="11ce7-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11ce7-134">OUTPUTS</span></span>

### <span data-ttu-id="11ce7-135">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. datafactors. MODELES. PSHub]</span><span class="sxs-lookup"><span data-stu-id="11ce7-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="11ce7-136">Microsoft. Azure. Commands. datafactors. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="11ce7-136">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="11ce7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11ce7-137">NOTES</span></span>
* <span data-ttu-id="11ce7-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="11ce7-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="11ce7-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11ce7-139">RELATED LINKS</span></span>

[<span data-ttu-id="11ce7-140">Nowe — AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="11ce7-140">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="11ce7-141">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="11ce7-141">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


