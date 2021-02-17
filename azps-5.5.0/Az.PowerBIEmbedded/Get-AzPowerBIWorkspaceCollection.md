---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183963"
---
# <span data-ttu-id="69707-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="69707-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="69707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69707-102">SYNOPSIS</span></span>
<span data-ttu-id="69707-103">Pobiera kolekcje obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="69707-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="69707-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69707-104">SYNTAX</span></span>

### <span data-ttu-id="69707-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="69707-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69707-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69707-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69707-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="69707-107">DESCRIPTION</span></span>
<span data-ttu-id="69707-108">Polecenie **cmdlet Get-AzPowerBIWorkspaceCollection** pobiera kolekcje obszarów roboczych usługi Power BI w Twojej grupie subskrypcji i zasobów platformy Azure lub według nazwy kolekcji.</span><span class="sxs-lookup"><span data-stu-id="69707-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="69707-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69707-109">EXAMPLES</span></span>

### <span data-ttu-id="69707-110">Przykład 1. Uzyskiwanie wszystkich kolekcji obszarów roboczych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="69707-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="69707-111">To polecenie pobiera kolekcje obszarów roboczych, które należą do grupy zasobów o nazwie Grupa Zasobów17.</span><span class="sxs-lookup"><span data-stu-id="69707-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="69707-112">Przykład 2. Uzyskiwanie kolekcji obszarów roboczych przy użyciu jej nazwy</span><span class="sxs-lookup"><span data-stu-id="69707-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="69707-113">To polecenie pobiera kolekcję obszaru roboczego o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="69707-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="69707-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69707-114">PARAMETERS</span></span>

### <span data-ttu-id="69707-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69707-115">-DefaultProfile</span></span>
<span data-ttu-id="69707-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="69707-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69707-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69707-117">-ResourceGroupName</span></span>
<span data-ttu-id="69707-118">Określa nazwę grupy zasobów, z której to polecenie cmdlet pobiera kolekcje obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="69707-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="69707-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="69707-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="69707-120">Określa nazwę zbioru obszarów roboczych usługi Power BI, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69707-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69707-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69707-121">CommonParameters</span></span>
<span data-ttu-id="69707-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69707-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69707-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69707-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69707-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69707-124">INPUTS</span></span>

### <span data-ttu-id="69707-125">System.String</span><span class="sxs-lookup"><span data-stu-id="69707-125">System.String</span></span>

## <span data-ttu-id="69707-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69707-126">OUTPUTS</span></span>

### <span data-ttu-id="69707-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="69707-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="69707-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69707-128">NOTES</span></span>

## <span data-ttu-id="69707-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69707-129">RELATED LINKS</span></span>

[<span data-ttu-id="69707-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="69707-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="69707-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="69707-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


