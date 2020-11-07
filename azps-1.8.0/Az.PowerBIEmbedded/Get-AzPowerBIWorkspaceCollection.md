---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 19b1d1b0da719167d53739a8c92a97121656aa9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708778"
---
# <span data-ttu-id="61655-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="61655-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="61655-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61655-102">SYNOPSIS</span></span>
<span data-ttu-id="61655-103">Pobiera kolekcje obszaru roboczego usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="61655-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="61655-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61655-104">SYNTAX</span></span>

### <span data-ttu-id="61655-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="61655-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61655-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61655-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61655-107">Opis</span><span class="sxs-lookup"><span data-stu-id="61655-107">DESCRIPTION</span></span>
<span data-ttu-id="61655-108">Polecenie cmdlet **Get-AzPowerBIWorkspaceCollection** pobiera kolekcje obszarów roboczych usługi Power BI w usłudze subskrypcji platformy Azure oraz w grupie zasobów lub według nazwy kolekcji.</span><span class="sxs-lookup"><span data-stu-id="61655-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="61655-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61655-109">EXAMPLES</span></span>

### <span data-ttu-id="61655-110">Przykład 1: pobieranie wszystkich kolekcji obszarów roboczych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="61655-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="61655-111">To polecenie pobiera kolekcje obszarów roboczych należące do grupy zasobów o nazwie ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="61655-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="61655-112">Przykład 2: uzyskiwanie kolekcji obszarów roboczych przy użyciu jej nazwy</span><span class="sxs-lookup"><span data-stu-id="61655-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="61655-113">To polecenie pobiera kolekcję obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="61655-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="61655-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61655-114">PARAMETERS</span></span>

### <span data-ttu-id="61655-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61655-115">-DefaultProfile</span></span>
<span data-ttu-id="61655-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="61655-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61655-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61655-117">-ResourceGroupName</span></span>
<span data-ttu-id="61655-118">Określa nazwę grupy zasobów, z której ten polecenie cmdlet pobiera kolekcje obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="61655-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="61655-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="61655-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="61655-120">Określa nazwę kolekcji obszaru roboczego usługi Power BI, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61655-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="61655-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61655-121">CommonParameters</span></span>
<span data-ttu-id="61655-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61655-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61655-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61655-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61655-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61655-124">INPUTS</span></span>

### <span data-ttu-id="61655-125">System. String</span><span class="sxs-lookup"><span data-stu-id="61655-125">System.String</span></span>

## <span data-ttu-id="61655-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61655-126">OUTPUTS</span></span>

### <span data-ttu-id="61655-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="61655-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="61655-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61655-128">NOTES</span></span>

## <span data-ttu-id="61655-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61655-129">RELATED LINKS</span></span>

[<span data-ttu-id="61655-130">Nowe — AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="61655-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="61655-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="61655-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


