---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7d7fefad86534cd2614312b21bd3ac392050e1b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543548"
---
# <span data-ttu-id="0828b-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0828b-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="0828b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0828b-102">SYNOPSIS</span></span>
<span data-ttu-id="0828b-103">Pobiera kolekcje obszaru roboczego usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="0828b-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0828b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0828b-104">SYNTAX</span></span>

### <span data-ttu-id="0828b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0828b-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0828b-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0828b-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0828b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0828b-107">DESCRIPTION</span></span>
<span data-ttu-id="0828b-108">Polecenie cmdlet **Get-AzureRmPowerBIWorkspaceCollection** pobiera kolekcje obszarów roboczych usługi Power BI w usłudze subskrypcji platformy Azure oraz w grupie zasobów lub według nazwy kolekcji.</span><span class="sxs-lookup"><span data-stu-id="0828b-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="0828b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0828b-109">EXAMPLES</span></span>

### <span data-ttu-id="0828b-110">Przykład 1: pobieranie wszystkich kolekcji obszarów roboczych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="0828b-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="0828b-111">To polecenie pobiera kolekcje obszarów roboczych należące do grupy zasobów o nazwie ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="0828b-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="0828b-112">Przykład 2: uzyskiwanie kolekcji obszarów roboczych przy użyciu jej nazwy</span><span class="sxs-lookup"><span data-stu-id="0828b-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0828b-113">To polecenie pobiera kolekcję obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0828b-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0828b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0828b-114">PARAMETERS</span></span>

### <span data-ttu-id="0828b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0828b-115">-DefaultProfile</span></span>
<span data-ttu-id="0828b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0828b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0828b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0828b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0828b-118">Określa nazwę grupy zasobów, z której ten polecenie cmdlet pobiera kolekcje obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="0828b-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0828b-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0828b-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0828b-120">Określa nazwę kolekcji obszaru roboczego usługi Power BI, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0828b-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0828b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0828b-121">CommonParameters</span></span>
<span data-ttu-id="0828b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0828b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0828b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0828b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0828b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0828b-124">INPUTS</span></span>

### <span data-ttu-id="0828b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0828b-125">System.String</span></span>

## <span data-ttu-id="0828b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0828b-126">OUTPUTS</span></span>

### <span data-ttu-id="0828b-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0828b-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="0828b-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0828b-128">NOTES</span></span>

## <span data-ttu-id="0828b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0828b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0828b-130">Nowe — AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0828b-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="0828b-131">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0828b-131">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


