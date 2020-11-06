---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 59f1eabbadda682c87917f41d96959c691b9e593
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551068"
---
# <span data-ttu-id="1b064-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b064-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="1b064-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b064-102">SYNOPSIS</span></span>
<span data-ttu-id="1b064-103">Usuwa fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="1b064-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b064-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b064-104">SYNTAX</span></span>

### <span data-ttu-id="1b064-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1b064-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b064-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b064-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b064-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1b064-107">DESCRIPTION</span></span>
<span data-ttu-id="1b064-108">Polecenie cmdlet **Remove-AzureRmDataFactory** umożliwia usunięcie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1b064-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="1b064-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b064-109">EXAMPLES</span></span>

### <span data-ttu-id="1b064-110">Przykład 1: usuwanie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="1b064-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1b064-111">To polecenie usuwa fabrykę danych o nazwie WikiADF z grupy zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="1b064-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="1b064-112">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="1b064-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="1b064-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b064-113">PARAMETERS</span></span>

### <span data-ttu-id="1b064-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b064-114">-DataFactory</span></span>
<span data-ttu-id="1b064-115">Określa obiekt **PSDataFactory** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1b064-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="1b064-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1b064-116">-Force</span></span>
<span data-ttu-id="1b064-117">Wskazuje, że to polecenie cmdlet usunie fabrykę danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1b064-117">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1b064-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b064-118">-Name</span></span>
<span data-ttu-id="1b064-119">Określa nazwę fabryki danych, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="1b064-119">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b064-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b064-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b064-121">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b064-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b064-122">To polecenie cmdlet umożliwia usunięcie fabryki danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1b064-122">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b064-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b064-123">-Confirm</span></span>
<span data-ttu-id="1b064-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b064-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b064-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b064-125">-WhatIf</span></span>
<span data-ttu-id="1b064-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b064-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b064-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b064-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b064-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b064-128">-DefaultProfile</span></span>
<span data-ttu-id="1b064-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b064-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b064-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b064-130">CommonParameters</span></span>
<span data-ttu-id="1b064-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b064-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b064-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b064-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b064-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b064-133">INPUTS</span></span>

## <span data-ttu-id="1b064-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b064-134">OUTPUTS</span></span>

### <span data-ttu-id="1b064-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b064-135">System.Boolean</span></span>

## <span data-ttu-id="1b064-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b064-136">NOTES</span></span>
* <span data-ttu-id="1b064-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="1b064-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b064-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b064-138">RELATED LINKS</span></span>

[<span data-ttu-id="1b064-139">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b064-139">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="1b064-140">Nowe — AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b064-140">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


