---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372337"
---
# <span data-ttu-id="8228f-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8228f-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="8228f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8228f-102">SYNOPSIS</span></span>
<span data-ttu-id="8228f-103">Usuwa połączoną usługę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8228f-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="8228f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8228f-104">SYNTAX</span></span>

### <span data-ttu-id="8228f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8228f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8228f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8228f-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8228f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8228f-107">DESCRIPTION</span></span>
<span data-ttu-id="8228f-108">Polecenie cmdlet **Remove-AzDataFactoryLinkedService** umożliwia usunięcie połączonej usługi z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8228f-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="8228f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8228f-109">EXAMPLES</span></span>

### <span data-ttu-id="8228f-110">Przykład 1: usuwanie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="8228f-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="8228f-111">To polecenie powoduje usunięcie połączonej usługi o nazwie LinkedServiceTest z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8228f-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="8228f-112">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="8228f-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="8228f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8228f-113">PARAMETERS</span></span>

### <span data-ttu-id="8228f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8228f-114">-DataFactory</span></span>
<span data-ttu-id="8228f-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="8228f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8228f-116">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8228f-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8228f-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8228f-117">-DataFactoryName</span></span>
<span data-ttu-id="8228f-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="8228f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8228f-119">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8228f-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8228f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8228f-120">-DefaultProfile</span></span>
<span data-ttu-id="8228f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8228f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8228f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8228f-122">-Force</span></span>
<span data-ttu-id="8228f-123">Wskazuje, że to polecenie cmdlet usunie połączoną usługę bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8228f-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8228f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8228f-124">-Name</span></span>
<span data-ttu-id="8228f-125">Określa nazwę połączonej usługi, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="8228f-125">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="8228f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8228f-126">-ResourceGroupName</span></span>
<span data-ttu-id="8228f-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8228f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8228f-128">To polecenie cmdlet powoduje usunięcie połączonej usługi z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8228f-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8228f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8228f-129">-Confirm</span></span>
<span data-ttu-id="8228f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8228f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8228f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8228f-131">-WhatIf</span></span>
<span data-ttu-id="8228f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8228f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8228f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8228f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8228f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8228f-134">CommonParameters</span></span>
<span data-ttu-id="8228f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8228f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8228f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8228f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8228f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8228f-137">INPUTS</span></span>

### <span data-ttu-id="8228f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8228f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8228f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8228f-139">System.String</span></span>

## <span data-ttu-id="8228f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8228f-140">OUTPUTS</span></span>

### <span data-ttu-id="8228f-141">System. void</span><span class="sxs-lookup"><span data-stu-id="8228f-141">System.Void</span></span>

## <span data-ttu-id="8228f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8228f-142">NOTES</span></span>
* <span data-ttu-id="8228f-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="8228f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8228f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8228f-144">RELATED LINKS</span></span>

[<span data-ttu-id="8228f-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8228f-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="8228f-146">Nowe — AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8228f-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


