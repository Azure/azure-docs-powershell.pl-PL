---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 0f8bd59f6215a2f9cc2bdbcc993da0cb373f70af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705973"
---
# <span data-ttu-id="de7dc-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="de7dc-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="de7dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="de7dc-103">Usuwa bramę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="de7dc-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="de7dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de7dc-104">SYNTAX</span></span>

### <span data-ttu-id="de7dc-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de7dc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de7dc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="de7dc-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de7dc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="de7dc-107">DESCRIPTION</span></span>
<span data-ttu-id="de7dc-108">Polecenie cmdlet **Remove-AzDataFactoryGateway** usuwa określoną bramę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="de7dc-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="de7dc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de7dc-109">EXAMPLES</span></span>

### <span data-ttu-id="de7dc-110">Przykład 1: usuwanie bramy</span><span class="sxs-lookup"><span data-stu-id="de7dc-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="de7dc-111">To polecenie usuwa bramę o nazwie ContosoGateway z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="de7dc-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="de7dc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de7dc-112">PARAMETERS</span></span>

### <span data-ttu-id="de7dc-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="de7dc-113">-DataFactory</span></span>
<span data-ttu-id="de7dc-114">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="de7dc-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="de7dc-115">To polecenie cmdlet umożliwia usunięcie bramy z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="de7dc-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="de7dc-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="de7dc-116">-DataFactoryName</span></span>
<span data-ttu-id="de7dc-117">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="de7dc-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="de7dc-118">To polecenie cmdlet umożliwia usunięcie bramy z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="de7dc-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="de7dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7dc-119">-DefaultProfile</span></span>
<span data-ttu-id="de7dc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="de7dc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de7dc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="de7dc-121">-Force</span></span>
<span data-ttu-id="de7dc-122">Wskazuje, że to polecenie cmdlet usunie bramę bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="de7dc-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="de7dc-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de7dc-123">-Name</span></span>
<span data-ttu-id="de7dc-124">Określa nazwę bramy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="de7dc-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="de7dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de7dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="de7dc-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de7dc-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="de7dc-127">To polecenie cmdlet umożliwia usunięcie bramy należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="de7dc-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="de7dc-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de7dc-128">-Confirm</span></span>
<span data-ttu-id="de7dc-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de7dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de7dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de7dc-130">-WhatIf</span></span>
<span data-ttu-id="de7dc-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de7dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de7dc-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de7dc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de7dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7dc-133">CommonParameters</span></span>
<span data-ttu-id="de7dc-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de7dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7dc-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de7dc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7dc-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de7dc-136">INPUTS</span></span>

### <span data-ttu-id="de7dc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="de7dc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="de7dc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="de7dc-138">System.String</span></span>

## <span data-ttu-id="de7dc-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de7dc-139">OUTPUTS</span></span>

### <span data-ttu-id="de7dc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de7dc-140">System.Boolean</span></span>

## <span data-ttu-id="de7dc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de7dc-141">NOTES</span></span>
* <span data-ttu-id="de7dc-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="de7dc-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="de7dc-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de7dc-143">RELATED LINKS</span></span>

[<span data-ttu-id="de7dc-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="de7dc-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="de7dc-145">Nowe — AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="de7dc-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="de7dc-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="de7dc-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


