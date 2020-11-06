---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: d92cb12f051095a7e5de47d9c12b2c2329841bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546244"
---
# <span data-ttu-id="3d63a-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="3d63a-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="3d63a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d63a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d63a-103">Tworzy centrum dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d63a-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d63a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d63a-104">SYNTAX</span></span>

### <span data-ttu-id="3d63a-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3d63a-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d63a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3d63a-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d63a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3d63a-107">DESCRIPTION</span></span>
<span data-ttu-id="3d63a-108">Polecenie cmdlet **New-AzureRmDataFactoryHub** tworzy centrum danych usługi Azure Data Factory w określonej grupie zasobów platformy Azure i w określonej fabryce danych z określoną definicją pliku.</span><span class="sxs-lookup"><span data-stu-id="3d63a-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="3d63a-109">Po utworzeniu centrum możesz używać go do przechowywania połączonych usług i zarządzania nimi w grupie, a także do koncentratora możesz dodać rurociągi.</span><span class="sxs-lookup"><span data-stu-id="3d63a-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="3d63a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d63a-110">EXAMPLES</span></span>

### <span data-ttu-id="3d63a-111">Przykład 1. Tworzenie centrum</span><span class="sxs-lookup"><span data-stu-id="3d63a-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="3d63a-112">To polecenie tworzy centrum o nazwie ContosoDataHub w grupie zasób ADFResourceGroup i fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="3d63a-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="3d63a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d63a-113">PARAMETERS</span></span>

### <span data-ttu-id="3d63a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d63a-114">-DataFactory</span></span>
<span data-ttu-id="3d63a-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="3d63a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3d63a-116">To polecenie cmdlet tworzy centrum dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3d63a-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d63a-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3d63a-117">-DataFactoryName</span></span>
<span data-ttu-id="3d63a-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3d63a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3d63a-119">To polecenie cmdlet tworzy centrum dla fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3d63a-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d63a-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="3d63a-120">-File</span></span>
<span data-ttu-id="3d63a-121">Określa pełną ścieżkę do pliku notacji JavaScript (kod JSON) zawierającego opis centrum.</span><span class="sxs-lookup"><span data-stu-id="3d63a-121">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="3d63a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3d63a-122">-Force</span></span>
<span data-ttu-id="3d63a-123">Wskazuje, że ten aplet polecenia zamieni istniejący koncentrator bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3d63a-123">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3d63a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d63a-124">-Name</span></span>
<span data-ttu-id="3d63a-125">Określa nazwę koncentratora, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="3d63a-125">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="3d63a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d63a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d63a-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d63a-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3d63a-128">To polecenie cmdlet powoduje utworzenie centrum należącego do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3d63a-128">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d63a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d63a-129">-Confirm</span></span>
<span data-ttu-id="3d63a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d63a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d63a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d63a-131">-WhatIf</span></span>
<span data-ttu-id="3d63a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d63a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d63a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d63a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d63a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d63a-134">-DefaultProfile</span></span>
<span data-ttu-id="3d63a-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d63a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d63a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d63a-136">CommonParameters</span></span>
<span data-ttu-id="3d63a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d63a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d63a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d63a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d63a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d63a-139">INPUTS</span></span>

## <span data-ttu-id="3d63a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d63a-140">OUTPUTS</span></span>

### <span data-ttu-id="3d63a-141">Microsoft. Azure. Commands. datafactors. models. PSHub</span><span class="sxs-lookup"><span data-stu-id="3d63a-141">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="3d63a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d63a-142">NOTES</span></span>
* <span data-ttu-id="3d63a-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="3d63a-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3d63a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d63a-144">RELATED LINKS</span></span>

[<span data-ttu-id="3d63a-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="3d63a-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="3d63a-146">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="3d63a-146">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


