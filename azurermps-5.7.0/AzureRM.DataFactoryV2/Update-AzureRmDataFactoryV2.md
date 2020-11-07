---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: d7173b75d9796eeab974973f9f997d5b7cb72b49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717338"
---
# <span data-ttu-id="7d6af-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7d6af-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="7d6af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d6af-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6af-103">Aktualizuje właściwości fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7d6af-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d6af-104">SYNTAX</span></span>

### <span data-ttu-id="7d6af-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d6af-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6af-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7d6af-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6af-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6af-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6af-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d6af-108">DESCRIPTION</span></span>
<span data-ttu-id="7d6af-109">Polecenie cmdlet **Update-AzureRmDataFactoryV2** aktualizuje znaczniki lub właściwości tożsamości fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7d6af-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="7d6af-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d6af-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6af-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d6af-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="7d6af-112">To polecenie aktualizuje znaczniki WikiADF Factory na słownik zawierający znacznik o nazwie myNewTagName z wartością myTagValue.</span><span class="sxs-lookup"><span data-stu-id="7d6af-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="7d6af-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d6af-113">PARAMETERS</span></span>

### <span data-ttu-id="7d6af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6af-114">-DefaultProfile</span></span>
<span data-ttu-id="7d6af-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6af-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d6af-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7d6af-116">-InputObject</span></span>
<span data-ttu-id="7d6af-117">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7d6af-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6af-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d6af-118">-Name</span></span>
<span data-ttu-id="7d6af-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7d6af-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6af-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d6af-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d6af-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6af-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6af-122">-ResourceId</span></span>
<span data-ttu-id="7d6af-123">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6af-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6af-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d6af-124">-Tag</span></span>
<span data-ttu-id="7d6af-125">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7d6af-125">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6af-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d6af-126">-Confirm</span></span>
<span data-ttu-id="7d6af-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6af-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6af-128">-WhatIf</span></span>
<span data-ttu-id="7d6af-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6af-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d6af-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d6af-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6af-131">CommonParameters</span></span>
<span data-ttu-id="7d6af-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6af-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6af-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d6af-134">INPUTS</span></span>

### <span data-ttu-id="7d6af-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7d6af-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="7d6af-136">System. String Microsoft. Azure. Management. DataFactory. models. FactoryIdentity</span><span class="sxs-lookup"><span data-stu-id="7d6af-136">System.String Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity</span></span>

## <span data-ttu-id="7d6af-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d6af-137">OUTPUTS</span></span>

### <span data-ttu-id="7d6af-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7d6af-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7d6af-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d6af-139">NOTES</span></span>

## <span data-ttu-id="7d6af-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d6af-140">RELATED LINKS</span></span>

