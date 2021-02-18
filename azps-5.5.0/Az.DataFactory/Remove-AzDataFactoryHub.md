---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 12a18c62d3cc3412726df323bd48acd86ed7b1fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181010"
---
# <span data-ttu-id="f2975-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f2975-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="f2975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2975-102">SYNOPSIS</span></span>
<span data-ttu-id="f2975-103">Usuwa centrum z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f2975-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="f2975-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2975-104">SYNTAX</span></span>

### <span data-ttu-id="f2975-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="f2975-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2975-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f2975-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2975-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2975-107">DESCRIPTION</span></span>
<span data-ttu-id="f2975-108">Polecenie **cmdlet Remove-AzDataFactoryHub** usuwa centrum z usługi Azure Data Factory w określonej grupie zasobów platformy Azure i w określonej fabrycznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="f2975-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="f2975-109">Usunięcie centrum spowoduje również usunięcie wszystkich połączonych usług i potoków w centrum.</span><span class="sxs-lookup"><span data-stu-id="f2975-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="f2975-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2975-110">EXAMPLES</span></span>

### <span data-ttu-id="f2975-111">Przykład 1. Usuwanie centrum</span><span class="sxs-lookup"><span data-stu-id="f2975-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="f2975-112">To polecenie usuwa centrum o nazwie ContosoDataHub z grupy zasobów platformy Azure O nazwie ADFResourceGroup i z fabryki danych O nazwie ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="f2975-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="f2975-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2975-113">PARAMETERS</span></span>

### <span data-ttu-id="f2975-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f2975-114">-DataFactory</span></span>
<span data-ttu-id="f2975-115">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="f2975-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f2975-116">To polecenie cmdlet usuwa centrum z fabryki danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f2975-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2975-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f2975-117">-DataFactoryName</span></span>
<span data-ttu-id="f2975-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f2975-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f2975-119">To polecenie cmdlet usuwa centrum z fabryki danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f2975-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2975-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2975-120">-DefaultProfile</span></span>
<span data-ttu-id="f2975-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f2975-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2975-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f2975-122">-Force</span></span>
<span data-ttu-id="f2975-123">Wskazuje, że to polecenie cmdlet usuwa centrum bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2975-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f2975-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2975-124">-Name</span></span>
<span data-ttu-id="f2975-125">Określa nazwę centrum do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f2975-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="f2975-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2975-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2975-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2975-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f2975-128">To polecenie cmdlet usuwa centrum z grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f2975-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2975-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2975-129">-Confirm</span></span>
<span data-ttu-id="f2975-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2975-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2975-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2975-131">-WhatIf</span></span>
<span data-ttu-id="f2975-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2975-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2975-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2975-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2975-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2975-134">CommonParameters</span></span>
<span data-ttu-id="f2975-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2975-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2975-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2975-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2975-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2975-137">INPUTS</span></span>

### <span data-ttu-id="f2975-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f2975-138">System.String</span></span>

### <span data-ttu-id="f2975-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f2975-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f2975-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2975-140">OUTPUTS</span></span>

### <span data-ttu-id="f2975-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2975-141">System.Boolean</span></span>

## <span data-ttu-id="f2975-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2975-142">NOTES</span></span>
* <span data-ttu-id="f2975-143">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="f2975-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f2975-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2975-144">RELATED LINKS</span></span>

[<span data-ttu-id="f2975-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f2975-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="f2975-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f2975-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


