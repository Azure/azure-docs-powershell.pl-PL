---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: c80716e53b6f3aec6c9196baebbcd333aed1582c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964826"
---
# <span data-ttu-id="bb0ca-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bb0ca-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="bb0ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0ca-103">Aktualizuje właściwości fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="bb0ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb0ca-104">SYNTAX</span></span>

### <span data-ttu-id="bb0ca-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="bb0ca-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb0ca-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bb0ca-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb0ca-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb0ca-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb0ca-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb0ca-108">DESCRIPTION</span></span>
<span data-ttu-id="bb0ca-109">Polecenie **cmdlet Update-AzDataFactoryV2** aktualizuje tagi lub właściwości tożsamości w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="bb0ca-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb0ca-110">EXAMPLES</span></span>

### <span data-ttu-id="bb0ca-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb0ca-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="bb0ca-112">To polecenie aktualizuje tagi dla fabrycznej witryny WikiADF do słownika zawierającego tag o nazwie myNewTagName z wartością myTagValue.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="bb0ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb0ca-113">PARAMETERS</span></span>

### <span data-ttu-id="bb0ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0ca-114">-DefaultProfile</span></span>
<span data-ttu-id="bb0ca-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb0ca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb0ca-116">-InputObject</span></span>
<span data-ttu-id="bb0ca-117">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ca-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb0ca-118">-Name</span></span>
<span data-ttu-id="bb0ca-119">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb0ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb0ca-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ca-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb0ca-122">-ResourceId</span></span>
<span data-ttu-id="bb0ca-123">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ca-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="bb0ca-124">-Tag</span></span>
<span data-ttu-id="bb0ca-125">Tagi fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="bb0ca-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb0ca-126">-Confirm</span></span>
<span data-ttu-id="bb0ca-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb0ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb0ca-128">-WhatIf</span></span>
<span data-ttu-id="bb0ca-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb0ca-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb0ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0ca-131">CommonParameters</span></span>
<span data-ttu-id="bb0ca-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb0ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0ca-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb0ca-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0ca-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb0ca-134">INPUTS</span></span>

### <span data-ttu-id="bb0ca-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bb0ca-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="bb0ca-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bb0ca-136">System.String</span></span>

## <span data-ttu-id="bb0ca-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb0ca-137">OUTPUTS</span></span>

### <span data-ttu-id="bb0ca-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bb0ca-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bb0ca-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb0ca-139">NOTES</span></span>

## <span data-ttu-id="bb0ca-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb0ca-140">RELATED LINKS</span></span>
