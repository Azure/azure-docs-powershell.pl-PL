---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186259"
---
# <span data-ttu-id="e897e-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="e897e-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="e897e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e897e-102">SYNOPSIS</span></span>
<span data-ttu-id="e897e-103">Tworzy centrum dla usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e897e-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="e897e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e897e-104">SYNTAX</span></span>

### <span data-ttu-id="e897e-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="e897e-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e897e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e897e-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e897e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e897e-107">DESCRIPTION</span></span>
<span data-ttu-id="e897e-108">Polecenie cmdlet **New-AzDataFactoryHub** tworzy centrum usługi Azure Data Factory w określonej grupie zasobów platformy Azure i w określonej fabrycznej bazie danych z określoną definicją pliku.</span><span class="sxs-lookup"><span data-stu-id="e897e-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="e897e-109">Po utworzeniu centrum można za jego pomocą przechowywać usługi połączone w grupie i zarządzać nimi, a także dodawać potoki do centrum.</span><span class="sxs-lookup"><span data-stu-id="e897e-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="e897e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e897e-110">EXAMPLES</span></span>

### <span data-ttu-id="e897e-111">Przykład 1. Tworzenie centrum</span><span class="sxs-lookup"><span data-stu-id="e897e-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="e897e-112">To polecenie tworzy centrum o nazwie ContosoDataHub w grupie zasobów ADFResourceGroup i w grupie danych O nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="e897e-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="e897e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e897e-113">PARAMETERS</span></span>

### <span data-ttu-id="e897e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e897e-114">-DataFactory</span></span>
<span data-ttu-id="e897e-115">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="e897e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e897e-116">To polecenie cmdlet tworzy centrum dla fabrycznych danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e897e-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e897e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e897e-117">-DataFactoryName</span></span>
<span data-ttu-id="e897e-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e897e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e897e-119">To polecenie cmdlet tworzy centrum dla fabrycznych danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e897e-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e897e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e897e-120">-DefaultProfile</span></span>
<span data-ttu-id="e897e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e897e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e897e-122">— Plik</span><span class="sxs-lookup"><span data-stu-id="e897e-122">-File</span></span>
<span data-ttu-id="e897e-123">Określa pełną ścieżkę pliku JavaScript Object Notation (JSON) zawierającego opis centrum.</span><span class="sxs-lookup"><span data-stu-id="e897e-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="e897e-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e897e-124">-Force</span></span>
<span data-ttu-id="e897e-125">Wskazuje, że to polecenie cmdlet zastępuje istniejące centrum bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e897e-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e897e-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e897e-126">-Name</span></span>
<span data-ttu-id="e897e-127">Określa nazwę centrum do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="e897e-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="e897e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e897e-128">-ResourceGroupName</span></span>
<span data-ttu-id="e897e-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e897e-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e897e-130">To polecenie cmdlet tworzy centrum należące do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e897e-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e897e-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e897e-131">-Confirm</span></span>
<span data-ttu-id="e897e-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e897e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e897e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e897e-133">-WhatIf</span></span>
<span data-ttu-id="e897e-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e897e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e897e-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e897e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e897e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e897e-136">CommonParameters</span></span>
<span data-ttu-id="e897e-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e897e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e897e-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e897e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e897e-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e897e-139">INPUTS</span></span>

### <span data-ttu-id="e897e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e897e-140">System.String</span></span>

### <span data-ttu-id="e897e-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e897e-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="e897e-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e897e-142">OUTPUTS</span></span>

### <span data-ttu-id="e897e-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="e897e-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="e897e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e897e-144">NOTES</span></span>
* <span data-ttu-id="e897e-145">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="e897e-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e897e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e897e-146">RELATED LINKS</span></span>

[<span data-ttu-id="e897e-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="e897e-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="e897e-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="e897e-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


