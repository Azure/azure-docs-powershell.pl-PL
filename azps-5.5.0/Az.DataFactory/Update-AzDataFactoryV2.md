---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186226"
---
# <span data-ttu-id="d83c4-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d83c4-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="d83c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d83c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d83c4-103">Aktualizuje właściwości fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d83c4-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="d83c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d83c4-104">SYNTAX</span></span>

### <span data-ttu-id="d83c4-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="d83c4-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d83c4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d83c4-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d83c4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d83c4-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d83c4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d83c4-108">DESCRIPTION</span></span>
<span data-ttu-id="d83c4-109">Polecenie **cmdlet Update-AzDataFactoryV2** aktualizuje tagi lub właściwości tożsamości w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="d83c4-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="d83c4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d83c4-110">EXAMPLES</span></span>

### <span data-ttu-id="d83c4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d83c4-111">Example 1</span></span>
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

<span data-ttu-id="d83c4-112">To polecenie aktualizuje tagi dla fabrycznej witryny WikiADF do słownika zawierającego tag o nazwie myNewTagName z wartością myTagValue.</span><span class="sxs-lookup"><span data-stu-id="d83c4-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="d83c4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d83c4-113">PARAMETERS</span></span>

### <span data-ttu-id="d83c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83c4-114">-DefaultProfile</span></span>
<span data-ttu-id="d83c4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d83c4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d83c4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d83c4-116">-InputObject</span></span>
<span data-ttu-id="d83c4-117">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="d83c4-117">The data factory object.</span></span>

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

### <span data-ttu-id="d83c4-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d83c4-118">-Name</span></span>
<span data-ttu-id="d83c4-119">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="d83c4-119">The data factory name.</span></span>

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

### <span data-ttu-id="d83c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="d83c4-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d83c4-121">The resource group name.</span></span>

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

### <span data-ttu-id="d83c4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d83c4-122">-ResourceId</span></span>
<span data-ttu-id="d83c4-123">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="d83c4-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d83c4-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="d83c4-124">-Tag</span></span>
<span data-ttu-id="d83c4-125">Tagi fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d83c4-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="d83c4-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d83c4-126">-Confirm</span></span>
<span data-ttu-id="d83c4-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d83c4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d83c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d83c4-128">-WhatIf</span></span>
<span data-ttu-id="d83c4-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d83c4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d83c4-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d83c4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d83c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83c4-131">CommonParameters</span></span>
<span data-ttu-id="d83c4-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83c4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83c4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83c4-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d83c4-134">INPUTS</span></span>

### <span data-ttu-id="d83c4-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d83c4-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="d83c4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d83c4-136">System.String</span></span>

## <span data-ttu-id="d83c4-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d83c4-137">OUTPUTS</span></span>

### <span data-ttu-id="d83c4-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d83c4-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d83c4-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d83c4-139">NOTES</span></span>

## <span data-ttu-id="d83c4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d83c4-140">RELATED LINKS</span></span>
