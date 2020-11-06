---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: b781207bae8b967acadf4a9ef3ae50c5ffc9cfef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545768"
---
# <span data-ttu-id="26ab7-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="26ab7-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="26ab7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="26ab7-103">Usuwa bramę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="26ab7-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26ab7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26ab7-104">SYNTAX</span></span>

### <span data-ttu-id="26ab7-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26ab7-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26ab7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="26ab7-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26ab7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="26ab7-107">DESCRIPTION</span></span>
<span data-ttu-id="26ab7-108">Polecenie cmdlet **Remove-AzureRmDataFactoryGateway** usuwa określoną bramę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="26ab7-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="26ab7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26ab7-109">EXAMPLES</span></span>

### <span data-ttu-id="26ab7-110">Przykład 1: usuwanie bramy</span><span class="sxs-lookup"><span data-stu-id="26ab7-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="26ab7-111">To polecenie usuwa bramę o nazwie ContosoGateway z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="26ab7-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="26ab7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26ab7-112">PARAMETERS</span></span>

### <span data-ttu-id="26ab7-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="26ab7-113">-DataFactory</span></span>
<span data-ttu-id="26ab7-114">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="26ab7-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="26ab7-115">To polecenie cmdlet umożliwia usunięcie bramy z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="26ab7-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="26ab7-116">-DataFactoryName</span></span>
<span data-ttu-id="26ab7-117">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="26ab7-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="26ab7-118">To polecenie cmdlet umożliwia usunięcie bramy z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="26ab7-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ab7-119">-DefaultProfile</span></span>
<span data-ttu-id="26ab7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="26ab7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="26ab7-121">-Force</span></span>
<span data-ttu-id="26ab7-122">Wskazuje, że to polecenie cmdlet usunie bramę bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26ab7-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26ab7-123">-Name</span></span>
<span data-ttu-id="26ab7-124">Określa nazwę bramy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="26ab7-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26ab7-125">-ResourceGroupName</span></span>
<span data-ttu-id="26ab7-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26ab7-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="26ab7-127">To polecenie cmdlet umożliwia usunięcie bramy należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="26ab7-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26ab7-128">-Confirm</span></span>
<span data-ttu-id="26ab7-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26ab7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26ab7-130">-WhatIf</span></span>
<span data-ttu-id="26ab7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26ab7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26ab7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26ab7-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ab7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ab7-133">CommonParameters</span></span>
<span data-ttu-id="26ab7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26ab7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ab7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ab7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ab7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26ab7-136">INPUTS</span></span>

### <span data-ttu-id="26ab7-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="26ab7-137">None</span></span>
<span data-ttu-id="26ab7-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="26ab7-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26ab7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26ab7-139">OUTPUTS</span></span>

### <span data-ttu-id="26ab7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26ab7-140">System.Boolean</span></span>

## <span data-ttu-id="26ab7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26ab7-141">NOTES</span></span>
* <span data-ttu-id="26ab7-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="26ab7-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26ab7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26ab7-143">RELATED LINKS</span></span>

[<span data-ttu-id="26ab7-144">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="26ab7-144">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="26ab7-145">Nowe — AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="26ab7-145">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="26ab7-146">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="26ab7-146">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


