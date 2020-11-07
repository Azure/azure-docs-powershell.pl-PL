---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718602"
---
# <span data-ttu-id="79a79-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="79a79-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="79a79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79a79-102">SYNOPSIS</span></span>
<span data-ttu-id="79a79-103">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="79a79-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79a79-104">SYNTAX</span></span>

### <span data-ttu-id="79a79-105">DevSpacesControllerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79a79-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a79-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a79-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a79-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a79-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a79-108">Opis</span><span class="sxs-lookup"><span data-stu-id="79a79-108">DESCRIPTION</span></span>
<span data-ttu-id="79a79-109">Zaktualizuj kontroler DevSpaces, aby dodać tagi.</span><span class="sxs-lookup"><span data-stu-id="79a79-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="79a79-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79a79-110">EXAMPLES</span></span>

### <span data-ttu-id="79a79-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79a79-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="79a79-112">Znakowanie DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="79a79-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="79a79-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79a79-113">PARAMETERS</span></span>

### <span data-ttu-id="79a79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a79-114">-DefaultProfile</span></span>
<span data-ttu-id="79a79-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79a79-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a79-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79a79-116">-InputObject</span></span>
<span data-ttu-id="79a79-117">Obiekt PSController, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="79a79-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79a79-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79a79-118">-Name</span></span>
<span data-ttu-id="79a79-119">Nazwa kontrolera DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="79a79-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a79-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a79-120">-ResourceGroupName</span></span>
<span data-ttu-id="79a79-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="79a79-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a79-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79a79-122">-ResourceId</span></span>
<span data-ttu-id="79a79-123">Identyfikator zasobu DevSpaces</span><span class="sxs-lookup"><span data-stu-id="79a79-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a79-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="79a79-124">-Tag</span></span>
<span data-ttu-id="79a79-125">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="79a79-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a79-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79a79-126">-Confirm</span></span>
<span data-ttu-id="79a79-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a79-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a79-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a79-128">-WhatIf</span></span>
<span data-ttu-id="79a79-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a79-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a79-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79a79-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a79-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a79-131">CommonParameters</span></span>
<span data-ttu-id="79a79-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a79-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a79-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a79-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a79-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79a79-134">INPUTS</span></span>

### <span data-ttu-id="79a79-135">System. String</span><span class="sxs-lookup"><span data-stu-id="79a79-135">System.String</span></span>

### <span data-ttu-id="79a79-136">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="79a79-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="79a79-137">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79a79-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="79a79-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79a79-138">OUTPUTS</span></span>

### <span data-ttu-id="79a79-139">Microsoft. Azure. Commands. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="79a79-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="79a79-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79a79-140">NOTES</span></span>

## <span data-ttu-id="79a79-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79a79-141">RELATED LINKS</span></span>
