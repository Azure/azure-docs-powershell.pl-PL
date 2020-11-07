---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 09e78957b3eef48731f2226a0737d0017c1e9b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717449"
---
# <span data-ttu-id="06e5e-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="06e5e-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="06e5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="06e5e-103">Usuwa centrum z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="06e5e-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06e5e-104">SYNTAX</span></span>

### <span data-ttu-id="06e5e-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06e5e-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06e5e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="06e5e-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e5e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="06e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="06e5e-108">Polecenie cmdlet **Remove-AzureRmDataFactoryHub** usuwa centrum z usługi Azure Data Factory w określonej grupie zasobów platformy Azure i w określonej fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="06e5e-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="06e5e-109">Jeśli usuniesz koncentrator, wszystkie połączone usługi i rurociągi w centrum zostaną również usunięte.</span><span class="sxs-lookup"><span data-stu-id="06e5e-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="06e5e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06e5e-110">EXAMPLES</span></span>

### <span data-ttu-id="06e5e-111">Przykład 1: usuwanie centrum</span><span class="sxs-lookup"><span data-stu-id="06e5e-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="06e5e-112">To polecenie usuwa centrum o nazwie ContosoDataHub z grupy zasobów platformy Azure o nazwie ADFResourceGroup i fabryki danych o nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="06e5e-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="06e5e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06e5e-113">PARAMETERS</span></span>

### <span data-ttu-id="06e5e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="06e5e-114">-DataFactory</span></span>
<span data-ttu-id="06e5e-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="06e5e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="06e5e-116">To polecenie cmdlet umożliwia usunięcie koncentratora z fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="06e5e-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="06e5e-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="06e5e-117">-DataFactoryName</span></span>
<span data-ttu-id="06e5e-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="06e5e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="06e5e-119">To polecenie cmdlet umożliwia usunięcie koncentratora z fabryki danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="06e5e-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="06e5e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e5e-120">-DefaultProfile</span></span>
<span data-ttu-id="06e5e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="06e5e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06e5e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="06e5e-122">-Force</span></span>
<span data-ttu-id="06e5e-123">Wskazuje, że to polecenie cmdlet usunie centrum bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06e5e-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="06e5e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06e5e-124">-Name</span></span>
<span data-ttu-id="06e5e-125">Określa nazwę koncentratora, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="06e5e-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="06e5e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e5e-126">-ResourceGroupName</span></span>
<span data-ttu-id="06e5e-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06e5e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="06e5e-128">To polecenie cmdlet umożliwia usunięcie koncentratora z grupy, którą określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="06e5e-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="06e5e-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06e5e-129">-Confirm</span></span>
<span data-ttu-id="06e5e-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e5e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e5e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e5e-131">-WhatIf</span></span>
<span data-ttu-id="06e5e-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e5e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e5e-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06e5e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e5e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e5e-134">CommonParameters</span></span>
<span data-ttu-id="06e5e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e5e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e5e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e5e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e5e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06e5e-137">INPUTS</span></span>

### <span data-ttu-id="06e5e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="06e5e-138">System.String</span></span>

### <span data-ttu-id="06e5e-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="06e5e-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="06e5e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06e5e-140">OUTPUTS</span></span>

### <span data-ttu-id="06e5e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06e5e-141">System.Boolean</span></span>

## <span data-ttu-id="06e5e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06e5e-142">NOTES</span></span>
* <span data-ttu-id="06e5e-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="06e5e-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="06e5e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06e5e-144">RELATED LINKS</span></span>

[<span data-ttu-id="06e5e-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="06e5e-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="06e5e-146">Nowe — AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="06e5e-146">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)


