---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306348"
---
# <span data-ttu-id="03f3e-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="03f3e-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="03f3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="03f3e-103">Pobiera informacje o koncentratorach w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="03f3e-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="03f3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03f3e-104">SYNTAX</span></span>

### <span data-ttu-id="03f3e-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03f3e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03f3e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="03f3e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03f3e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03f3e-107">DESCRIPTION</span></span>
<span data-ttu-id="03f3e-108">Polecenie cmdlet **Get-AzDataFactoryHub** pobiera informacje o koncentratorach w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="03f3e-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="03f3e-109">Jeśli określisz nazwę koncentratora, to polecenie cmdlet będzie pobierać informacje o tym koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="03f3e-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="03f3e-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich koncentratorach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="03f3e-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="03f3e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03f3e-111">EXAMPLES</span></span>

### <span data-ttu-id="03f3e-112">Przykład 1: pobieranie wszystkich koncentratorów danych</span><span class="sxs-lookup"><span data-stu-id="03f3e-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="03f3e-113">To polecenie pobiera wszystkie centra danych w grupie zasobów platformy Azure o nazwie ADFResourceGroup oraz fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="03f3e-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="03f3e-114">Przykład 2: uzyskiwanie określonego centrum danych</span><span class="sxs-lookup"><span data-stu-id="03f3e-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="03f3e-115">To polecenie pobiera informacje o centrum o nazwie MyDataHub w grupie zasobów platformy Azure o nazwie ADFResourceGroup i fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="03f3e-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="03f3e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03f3e-116">PARAMETERS</span></span>

### <span data-ttu-id="03f3e-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="03f3e-117">-DataFactory</span></span>
<span data-ttu-id="03f3e-118">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="03f3e-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="03f3e-119">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach w fabryce danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="03f3e-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="03f3e-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="03f3e-120">-DataFactoryName</span></span>
<span data-ttu-id="03f3e-121">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="03f3e-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="03f3e-122">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach w fabryce danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="03f3e-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="03f3e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f3e-123">-DefaultProfile</span></span>
<span data-ttu-id="03f3e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="03f3e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03f3e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03f3e-125">-Name</span></span>
<span data-ttu-id="03f3e-126">Określa nazwę centrum, o którym należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="03f3e-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="03f3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03f3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="03f3e-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="03f3e-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="03f3e-129">To polecenie cmdlet umożliwia pobieranie informacji o koncentratorach należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="03f3e-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="03f3e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f3e-130">CommonParameters</span></span>
<span data-ttu-id="03f3e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f3e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f3e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03f3e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f3e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03f3e-133">INPUTS</span></span>

### <span data-ttu-id="03f3e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="03f3e-134">System.String</span></span>

### <span data-ttu-id="03f3e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="03f3e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="03f3e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03f3e-136">OUTPUTS</span></span>

### <span data-ttu-id="03f3e-137">Microsoft. Azure. Commands. datafactors. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="03f3e-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="03f3e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03f3e-138">NOTES</span></span>
* <span data-ttu-id="03f3e-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="03f3e-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="03f3e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03f3e-140">RELATED LINKS</span></span>

[<span data-ttu-id="03f3e-141">Nowe — AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="03f3e-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="03f3e-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="03f3e-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


