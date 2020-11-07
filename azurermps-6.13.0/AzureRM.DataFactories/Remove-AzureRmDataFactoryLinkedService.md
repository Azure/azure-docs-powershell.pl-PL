---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7b4dd01a689e1ac7b87e1c83a1e19bbd0c8a86db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717450"
---
# <span data-ttu-id="98da0-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="98da0-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="98da0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98da0-102">SYNOPSIS</span></span>
<span data-ttu-id="98da0-103">Usuwa połączoną usługę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="98da0-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98da0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98da0-104">SYNTAX</span></span>

### <span data-ttu-id="98da0-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98da0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98da0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="98da0-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98da0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98da0-107">DESCRIPTION</span></span>
<span data-ttu-id="98da0-108">Polecenie cmdlet **Remove-AzureRmDataFactoryLinkedService** umożliwia usunięcie połączonej usługi z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="98da0-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="98da0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98da0-109">EXAMPLES</span></span>

### <span data-ttu-id="98da0-110">Przykład 1: usuwanie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="98da0-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="98da0-111">To polecenie powoduje usunięcie połączonej usługi o nazwie LinkedServiceTest z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="98da0-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="98da0-112">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="98da0-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="98da0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98da0-113">PARAMETERS</span></span>

### <span data-ttu-id="98da0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="98da0-114">-DataFactory</span></span>
<span data-ttu-id="98da0-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="98da0-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="98da0-116">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="98da0-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98da0-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="98da0-117">-DataFactoryName</span></span>
<span data-ttu-id="98da0-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="98da0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="98da0-119">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="98da0-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98da0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98da0-120">-DefaultProfile</span></span>
<span data-ttu-id="98da0-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="98da0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98da0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="98da0-122">-Force</span></span>
<span data-ttu-id="98da0-123">Wskazuje, że to polecenie cmdlet usunie połączoną usługę bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98da0-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="98da0-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98da0-124">-Name</span></span>
<span data-ttu-id="98da0-125">Określa nazwę połączonej usługi, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="98da0-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98da0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98da0-126">-ResourceGroupName</span></span>
<span data-ttu-id="98da0-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98da0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="98da0-128">To polecenie cmdlet powoduje usunięcie połączonej usługi z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="98da0-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="98da0-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98da0-129">-Confirm</span></span>
<span data-ttu-id="98da0-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98da0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98da0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98da0-131">-WhatIf</span></span>
<span data-ttu-id="98da0-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98da0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98da0-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98da0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98da0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98da0-134">CommonParameters</span></span>
<span data-ttu-id="98da0-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98da0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98da0-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98da0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98da0-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98da0-137">INPUTS</span></span>

### <span data-ttu-id="98da0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="98da0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="98da0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="98da0-139">System.String</span></span>

## <span data-ttu-id="98da0-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98da0-140">OUTPUTS</span></span>

### <span data-ttu-id="98da0-141">System. void</span><span class="sxs-lookup"><span data-stu-id="98da0-141">System.Void</span></span>

## <span data-ttu-id="98da0-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98da0-142">NOTES</span></span>
* <span data-ttu-id="98da0-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="98da0-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="98da0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98da0-144">RELATED LINKS</span></span>

[<span data-ttu-id="98da0-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="98da0-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="98da0-146">Nowe — AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="98da0-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


