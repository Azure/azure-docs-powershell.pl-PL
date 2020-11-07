---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 35287cf75c8fbcb726ace19abe6f7c6923b537df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717608"
---
# <span data-ttu-id="c052e-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c052e-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="c052e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c052e-102">SYNOPSIS</span></span>
<span data-ttu-id="c052e-103">Usuwa kolekcję obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="c052e-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c052e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c052e-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c052e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c052e-105">DESCRIPTION</span></span>
<span data-ttu-id="c052e-106">Polecenie cmdlet **Remove-AzureRmPowerBIWorkspaceCollection** usuwa kolekcję obszarów roboczych usługi Power BI z subskrypcji i grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c052e-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="c052e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c052e-107">EXAMPLES</span></span>

### <span data-ttu-id="c052e-108">Przykład 1: usuwanie kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="c052e-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c052e-109">To polecenie usuwa kolekcję obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c052e-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c052e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c052e-110">PARAMETERS</span></span>

### <span data-ttu-id="c052e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c052e-111">-DefaultProfile</span></span>
<span data-ttu-id="c052e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c052e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c052e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c052e-113">-ResourceGroupName</span></span>
<span data-ttu-id="c052e-114">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa kolekcję obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="c052e-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="c052e-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c052e-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c052e-116">Określa nazwę kolekcji obszaru roboczego usługi Power BI, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c052e-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c052e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c052e-117">-Confirm</span></span>
<span data-ttu-id="c052e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c052e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c052e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c052e-119">-WhatIf</span></span>
<span data-ttu-id="c052e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c052e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c052e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c052e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c052e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c052e-122">CommonParameters</span></span>
<span data-ttu-id="c052e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c052e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c052e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c052e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c052e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c052e-125">INPUTS</span></span>

### <span data-ttu-id="c052e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c052e-126">System.String</span></span>

## <span data-ttu-id="c052e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c052e-127">OUTPUTS</span></span>

### <span data-ttu-id="c052e-128">System. void</span><span class="sxs-lookup"><span data-stu-id="c052e-128">System.Void</span></span>

## <span data-ttu-id="c052e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c052e-129">NOTES</span></span>

## <span data-ttu-id="c052e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c052e-130">RELATED LINKS</span></span>

[<span data-ttu-id="c052e-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c052e-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="c052e-132">Nowe — AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c052e-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


