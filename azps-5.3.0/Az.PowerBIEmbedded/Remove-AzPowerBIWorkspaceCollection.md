---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490854"
---
# <span data-ttu-id="81edb-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="81edb-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="81edb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81edb-102">SYNOPSIS</span></span>
<span data-ttu-id="81edb-103">Usuwa kolekcję obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="81edb-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="81edb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81edb-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81edb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81edb-105">DESCRIPTION</span></span>
<span data-ttu-id="81edb-106">Polecenie cmdlet **Remove-AzPowerBIWorkspaceCollection** usuwa kolekcję obszarów roboczych usługi Power BI z subskrypcji i grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="81edb-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="81edb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81edb-107">EXAMPLES</span></span>

### <span data-ttu-id="81edb-108">Przykład 1: usuwanie kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="81edb-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="81edb-109">To polecenie usuwa kolekcję obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="81edb-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="81edb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81edb-110">PARAMETERS</span></span>

### <span data-ttu-id="81edb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81edb-111">-DefaultProfile</span></span>
<span data-ttu-id="81edb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="81edb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81edb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81edb-113">-ResourceGroupName</span></span>
<span data-ttu-id="81edb-114">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa kolekcję obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="81edb-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81edb-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="81edb-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="81edb-116">Określa nazwę kolekcji obszaru roboczego usługi Power BI, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81edb-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81edb-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81edb-117">-Confirm</span></span>
<span data-ttu-id="81edb-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81edb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81edb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81edb-119">-WhatIf</span></span>
<span data-ttu-id="81edb-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81edb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81edb-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81edb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81edb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81edb-122">CommonParameters</span></span>
<span data-ttu-id="81edb-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81edb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81edb-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81edb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81edb-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81edb-125">INPUTS</span></span>

### <span data-ttu-id="81edb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="81edb-126">System.String</span></span>

## <span data-ttu-id="81edb-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81edb-127">OUTPUTS</span></span>

### <span data-ttu-id="81edb-128">System. void</span><span class="sxs-lookup"><span data-stu-id="81edb-128">System.Void</span></span>

## <span data-ttu-id="81edb-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81edb-129">NOTES</span></span>

## <span data-ttu-id="81edb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81edb-130">RELATED LINKS</span></span>

[<span data-ttu-id="81edb-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="81edb-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="81edb-132">Nowe — AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="81edb-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


