---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 24c9f9631f1a37e218ff8ddf27ad0de54f2d9dbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975425"
---
# <span data-ttu-id="034da-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="034da-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="034da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034da-102">SYNOPSIS</span></span>
<span data-ttu-id="034da-103">Pobiera informacje o centrach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="034da-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="034da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="034da-104">SYNTAX</span></span>

### <span data-ttu-id="034da-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="034da-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="034da-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="034da-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="034da-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="034da-107">DESCRIPTION</span></span>
<span data-ttu-id="034da-108">Polecenie **cmdlet Get-AzDataFactoryHub** pobiera informacje o centrach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="034da-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="034da-109">Jeśli określisz nazwę centrum, to polecenie cmdlet pobiera informacje o tym centrum.</span><span class="sxs-lookup"><span data-stu-id="034da-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="034da-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich koncentratorach w factory danych.</span><span class="sxs-lookup"><span data-stu-id="034da-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="034da-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="034da-111">EXAMPLES</span></span>

### <span data-ttu-id="034da-112">Przykład 1. Uzyskiwanie wszystkich koncentratorów danych</span><span class="sxs-lookup"><span data-stu-id="034da-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="034da-113">To polecenie pobiera wszystkie koncentratory danych w grupie zasobów platformy Azure o nazwie ADFResourceGroup i factory data factory o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="034da-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="034da-114">Przykład 2. Uzyskiwanie określonego centrum danych</span><span class="sxs-lookup"><span data-stu-id="034da-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="034da-115">To polecenie pobiera informacje o centrum o nazwie MyDataHub w grupie zasobów platformy Azure o nazwie ADFResourceGroup i usłudze data factory o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="034da-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="034da-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="034da-116">PARAMETERS</span></span>

### <span data-ttu-id="034da-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="034da-117">-DataFactory</span></span>
<span data-ttu-id="034da-118">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="034da-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="034da-119">To polecenie cmdlet pobiera informacje o koncentratorach w zakładzie danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="034da-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="034da-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="034da-120">-DataFactoryName</span></span>
<span data-ttu-id="034da-121">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="034da-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="034da-122">To polecenie cmdlet pobiera informacje o koncentratorach w zakładzie danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="034da-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="034da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034da-123">-DefaultProfile</span></span>
<span data-ttu-id="034da-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="034da-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="034da-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="034da-125">-Name</span></span>
<span data-ttu-id="034da-126">Określa nazwę centrum, o którym mają być informacje.</span><span class="sxs-lookup"><span data-stu-id="034da-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="034da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034da-127">-ResourceGroupName</span></span>
<span data-ttu-id="034da-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="034da-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="034da-129">To polecenie cmdlet pobiera informacje o centrach należących do grupy, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="034da-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="034da-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034da-130">CommonParameters</span></span>
<span data-ttu-id="034da-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034da-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034da-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034da-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034da-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="034da-133">INPUTS</span></span>

### <span data-ttu-id="034da-134">System.String</span><span class="sxs-lookup"><span data-stu-id="034da-134">System.String</span></span>

### <span data-ttu-id="034da-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="034da-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="034da-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="034da-136">OUTPUTS</span></span>

### <span data-ttu-id="034da-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="034da-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="034da-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="034da-138">NOTES</span></span>
* <span data-ttu-id="034da-139">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="034da-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="034da-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="034da-140">RELATED LINKS</span></span>

[<span data-ttu-id="034da-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="034da-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="034da-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="034da-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


