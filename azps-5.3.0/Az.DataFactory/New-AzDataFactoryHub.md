---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501574"
---
# <span data-ttu-id="bba4f-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="bba4f-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="bba4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bba4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bba4f-103">Tworzy centrum dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bba4f-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="bba4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bba4f-104">SYNTAX</span></span>

### <span data-ttu-id="bba4f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bba4f-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bba4f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bba4f-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bba4f-107">DESCRIPTION</span></span>
<span data-ttu-id="bba4f-108">Polecenie cmdlet **New-AzDataFactoryHub** tworzy centrum danych usługi Azure Data Factory w określonej grupie zasobów platformy Azure i w określonej fabryce danych z określoną definicją pliku.</span><span class="sxs-lookup"><span data-stu-id="bba4f-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="bba4f-109">Po utworzeniu centrum możesz używać go do przechowywania połączonych usług i zarządzania nimi w grupie, a także do koncentratora możesz dodać rurociągi.</span><span class="sxs-lookup"><span data-stu-id="bba4f-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="bba4f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bba4f-110">EXAMPLES</span></span>

### <span data-ttu-id="bba4f-111">Przykład 1. Tworzenie centrum</span><span class="sxs-lookup"><span data-stu-id="bba4f-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="bba4f-112">To polecenie tworzy centrum o nazwie ContosoDataHub w grupie zasób ADFResourceGroup i fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="bba4f-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="bba4f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bba4f-113">PARAMETERS</span></span>

### <span data-ttu-id="bba4f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bba4f-114">-DataFactory</span></span>
<span data-ttu-id="bba4f-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="bba4f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bba4f-116">To polecenie cmdlet tworzy centrum dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bba4f-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bba4f-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bba4f-117">-DataFactoryName</span></span>
<span data-ttu-id="bba4f-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bba4f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bba4f-119">To polecenie cmdlet tworzy centrum dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bba4f-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bba4f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba4f-120">-DefaultProfile</span></span>
<span data-ttu-id="bba4f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bba4f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bba4f-122">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="bba4f-122">-File</span></span>
<span data-ttu-id="bba4f-123">Określa pełną ścieżkę do pliku notacji JavaScript (kod JSON) zawierającego opis centrum.</span><span class="sxs-lookup"><span data-stu-id="bba4f-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba4f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bba4f-124">-Force</span></span>
<span data-ttu-id="bba4f-125">Wskazuje, że ten aplet polecenia zamieni istniejący koncentrator bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bba4f-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bba4f-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bba4f-126">-Name</span></span>
<span data-ttu-id="bba4f-127">Określa nazwę koncentratora, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="bba4f-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="bba4f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba4f-128">-ResourceGroupName</span></span>
<span data-ttu-id="bba4f-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bba4f-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bba4f-130">To polecenie cmdlet powoduje utworzenie centrum należącego do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bba4f-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bba4f-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bba4f-131">-Confirm</span></span>
<span data-ttu-id="bba4f-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bba4f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba4f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba4f-133">-WhatIf</span></span>
<span data-ttu-id="bba4f-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bba4f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba4f-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bba4f-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba4f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba4f-136">CommonParameters</span></span>
<span data-ttu-id="bba4f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba4f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba4f-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba4f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba4f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bba4f-139">INPUTS</span></span>

### <span data-ttu-id="bba4f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bba4f-140">System.String</span></span>

### <span data-ttu-id="bba4f-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bba4f-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="bba4f-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bba4f-142">OUTPUTS</span></span>

### <span data-ttu-id="bba4f-143">Microsoft. Azure. Commands. datafactors. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="bba4f-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="bba4f-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bba4f-144">NOTES</span></span>
* <span data-ttu-id="bba4f-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="bba4f-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bba4f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bba4f-146">RELATED LINKS</span></span>

[<span data-ttu-id="bba4f-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="bba4f-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="bba4f-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="bba4f-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


