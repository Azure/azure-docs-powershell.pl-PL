---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 0136927eea72911e706c3e0062dbc444cf1f9b25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710097"
---
# <span data-ttu-id="eb9ba-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="eb9ba-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="eb9ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9ba-103">Usuwa centrum z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="eb9ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb9ba-104">SYNTAX</span></span>

### <span data-ttu-id="eb9ba-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eb9ba-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb9ba-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eb9ba-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb9ba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eb9ba-107">DESCRIPTION</span></span>
<span data-ttu-id="eb9ba-108">Polecenie cmdlet **Remove-AzDataFactoryHub** usuwa centrum z usługi Azure Data Factory w określonej grupie zasobów platformy Azure i w określonej fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="eb9ba-109">Jeśli usuniesz koncentrator, wszystkie połączone usługi i rurociągi w centrum zostaną również usunięte.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="eb9ba-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb9ba-110">EXAMPLES</span></span>

### <span data-ttu-id="eb9ba-111">Przykład 1: usuwanie centrum</span><span class="sxs-lookup"><span data-stu-id="eb9ba-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="eb9ba-112">To polecenie usuwa centrum o nazwie ContosoDataHub z grupy zasobów platformy Azure o nazwie ADFResourceGroup i fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="eb9ba-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb9ba-113">PARAMETERS</span></span>

### <span data-ttu-id="eb9ba-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="eb9ba-114">-DataFactory</span></span>
<span data-ttu-id="eb9ba-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="eb9ba-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="eb9ba-116">To polecenie cmdlet umożliwia usunięcie koncentratora z fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb9ba-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="eb9ba-117">-DataFactoryName</span></span>
<span data-ttu-id="eb9ba-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="eb9ba-119">To polecenie cmdlet umożliwia usunięcie koncentratora z fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb9ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9ba-120">-DefaultProfile</span></span>
<span data-ttu-id="eb9ba-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eb9ba-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb9ba-122">-Force</span><span class="sxs-lookup"><span data-stu-id="eb9ba-122">-Force</span></span>
<span data-ttu-id="eb9ba-123">Wskazuje, że to polecenie cmdlet usunie centrum bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="eb9ba-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eb9ba-124">-Name</span></span>
<span data-ttu-id="eb9ba-125">Określa nazwę koncentratora, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb9ba-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eb9ba-128">To polecenie cmdlet umożliwia usunięcie koncentratora z grupy, którą określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb9ba-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb9ba-129">-Confirm</span></span>
<span data-ttu-id="eb9ba-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb9ba-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb9ba-131">-WhatIf</span></span>
<span data-ttu-id="eb9ba-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb9ba-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb9ba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9ba-134">CommonParameters</span></span>
<span data-ttu-id="eb9ba-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9ba-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb9ba-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9ba-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb9ba-137">INPUTS</span></span>

### <span data-ttu-id="eb9ba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eb9ba-138">System.String</span></span>

### <span data-ttu-id="eb9ba-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb9ba-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="eb9ba-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb9ba-140">OUTPUTS</span></span>

### <span data-ttu-id="eb9ba-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb9ba-141">System.Boolean</span></span>

## <span data-ttu-id="eb9ba-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb9ba-142">NOTES</span></span>
* <span data-ttu-id="eb9ba-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="eb9ba-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eb9ba-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb9ba-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb9ba-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="eb9ba-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="eb9ba-146">Nowe — AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="eb9ba-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


