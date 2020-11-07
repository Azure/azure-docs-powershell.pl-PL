---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: d3ea4c3f221a3d05c9d43e780cde359ff36843f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717350"
---
# <span data-ttu-id="9d0f2-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9d0f2-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="9d0f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0f2-103">Usuwa połączoną usługę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d0f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d0f2-104">SYNTAX</span></span>

### <span data-ttu-id="9d0f2-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d0f2-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0f2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9d0f2-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d0f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d0f2-107">DESCRIPTION</span></span>
<span data-ttu-id="9d0f2-108">Polecenie cmdlet **Remove-AzureRmDataFactoryLinkedService** umożliwia usunięcie połączonej usługi z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="9d0f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d0f2-109">EXAMPLES</span></span>

### <span data-ttu-id="9d0f2-110">Przykład 1: usuwanie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="9d0f2-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="9d0f2-111">To polecenie powoduje usunięcie połączonej usługi o nazwie LinkedServiceTest z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="9d0f2-112">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="9d0f2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d0f2-113">PARAMETERS</span></span>

### <span data-ttu-id="9d0f2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9d0f2-114">-DataFactory</span></span>
<span data-ttu-id="9d0f2-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9d0f2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9d0f2-116">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d0f2-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9d0f2-117">-DataFactoryName</span></span>
<span data-ttu-id="9d0f2-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9d0f2-119">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d0f2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9d0f2-120">-Force</span></span>
<span data-ttu-id="9d0f2-121">Wskazuje, że to polecenie cmdlet usunie połączoną usługę bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-121">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9d0f2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d0f2-122">-Name</span></span>
<span data-ttu-id="9d0f2-123">Określa nazwę połączonej usługi, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-123">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="9d0f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d0f2-125">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9d0f2-126">To polecenie cmdlet powoduje usunięcie połączonej usługi z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-126">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d0f2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d0f2-127">-Confirm</span></span>
<span data-ttu-id="9d0f2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d0f2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d0f2-129">-WhatIf</span></span>
<span data-ttu-id="9d0f2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d0f2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d0f2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0f2-132">-DefaultProfile</span></span>
<span data-ttu-id="9d0f2-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d0f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0f2-134">CommonParameters</span></span>
<span data-ttu-id="9d0f2-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d0f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0f2-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d0f2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0f2-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d0f2-137">INPUTS</span></span>

## <span data-ttu-id="9d0f2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d0f2-138">OUTPUTS</span></span>

### <span data-ttu-id="9d0f2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d0f2-139">System.Boolean</span></span>

## <span data-ttu-id="9d0f2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d0f2-140">NOTES</span></span>
* <span data-ttu-id="9d0f2-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="9d0f2-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9d0f2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d0f2-142">RELATED LINKS</span></span>

[<span data-ttu-id="9d0f2-143">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9d0f2-143">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="9d0f2-144">Nowe — AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9d0f2-144">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


