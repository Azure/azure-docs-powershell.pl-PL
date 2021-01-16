---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327320"
---
# <span data-ttu-id="33f79-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="33f79-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="33f79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33f79-102">SYNOPSIS</span></span>
<span data-ttu-id="33f79-103">Usuwa fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="33f79-103">Removes a data factory.</span></span>

## <span data-ttu-id="33f79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33f79-104">SYNTAX</span></span>

### <span data-ttu-id="33f79-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33f79-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33f79-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="33f79-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33f79-107">Opis</span><span class="sxs-lookup"><span data-stu-id="33f79-107">DESCRIPTION</span></span>
<span data-ttu-id="33f79-108">Polecenie cmdlet **Remove-AzDataFactory** umożliwia usunięcie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="33f79-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="33f79-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33f79-109">EXAMPLES</span></span>

### <span data-ttu-id="33f79-110">Przykład 1: usuwanie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="33f79-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="33f79-111">To polecenie usuwa fabrykę danych o nazwie WikiADF z grupy zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="33f79-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="33f79-112">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="33f79-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="33f79-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33f79-113">PARAMETERS</span></span>

### <span data-ttu-id="33f79-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="33f79-114">-DataFactory</span></span>
<span data-ttu-id="33f79-115">Określa obiekt **PSDataFactory** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="33f79-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="33f79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f79-116">-DefaultProfile</span></span>
<span data-ttu-id="33f79-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="33f79-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33f79-118">-Force</span><span class="sxs-lookup"><span data-stu-id="33f79-118">-Force</span></span>
<span data-ttu-id="33f79-119">Wskazuje, że to polecenie cmdlet usunie fabrykę danych bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33f79-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="33f79-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33f79-120">-Name</span></span>
<span data-ttu-id="33f79-121">Określa nazwę fabryki danych, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="33f79-121">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="33f79-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33f79-122">-ResourceGroupName</span></span>
<span data-ttu-id="33f79-123">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33f79-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="33f79-124">To polecenie cmdlet umożliwia usunięcie fabryki danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="33f79-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="33f79-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33f79-125">-Confirm</span></span>
<span data-ttu-id="33f79-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33f79-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33f79-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f79-127">-WhatIf</span></span>
<span data-ttu-id="33f79-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33f79-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33f79-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33f79-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33f79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f79-130">CommonParameters</span></span>
<span data-ttu-id="33f79-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f79-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f79-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f79-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33f79-133">INPUTS</span></span>

### <span data-ttu-id="33f79-134">System. String</span><span class="sxs-lookup"><span data-stu-id="33f79-134">System.String</span></span>

### <span data-ttu-id="33f79-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="33f79-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="33f79-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33f79-136">OUTPUTS</span></span>

### <span data-ttu-id="33f79-137">System. void</span><span class="sxs-lookup"><span data-stu-id="33f79-137">System.Void</span></span>

## <span data-ttu-id="33f79-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33f79-138">NOTES</span></span>
* <span data-ttu-id="33f79-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="33f79-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="33f79-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33f79-140">RELATED LINKS</span></span>

[<span data-ttu-id="33f79-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="33f79-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="33f79-142">Nowe — AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="33f79-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


