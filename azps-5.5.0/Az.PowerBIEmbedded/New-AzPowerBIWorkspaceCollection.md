---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202139"
---
# <span data-ttu-id="8b5e1-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8b5e1-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="8b5e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5e1-103">Tworzy kolekcję obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="8b5e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b5e1-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b5e1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b5e1-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5e1-106">Polecenie cmdlet **New-AzPowerBIWorkspaceCollection** tworzy kolekcję obszaru roboczego usługi Power BI dla twojej subskrypcji platformy Azure w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="8b5e1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b5e1-107">EXAMPLES</span></span>

### <span data-ttu-id="8b5e1-108">Przykład 1. Tworzenie kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="8b5e1-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="8b5e1-109">To polecenie tworzy kolekcję obszaru roboczego o nazwie WCN11 w określonej grupie zasobów w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="8b5e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b5e1-110">PARAMETERS</span></span>

### <span data-ttu-id="8b5e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5e1-111">-DefaultProfile</span></span>
<span data-ttu-id="8b5e1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8b5e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b5e1-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b5e1-113">-Location</span></span>
<span data-ttu-id="8b5e1-114">Określa lokalizację platformy Azure, w której to polecenie cmdlet tworzy kolekcję obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5e1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b5e1-115">-ResourceGroupName</span></span>
<span data-ttu-id="8b5e1-116">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy kolekcję obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="8b5e1-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="8b5e1-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="8b5e1-118">Określa nazwę zbioru obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="8b5e1-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b5e1-119">-Confirm</span></span>
<span data-ttu-id="8b5e1-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b5e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b5e1-121">-WhatIf</span></span>
<span data-ttu-id="8b5e1-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b5e1-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b5e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5e1-124">CommonParameters</span></span>
<span data-ttu-id="8b5e1-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5e1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5e1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5e1-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b5e1-127">INPUTS</span></span>

### <span data-ttu-id="8b5e1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8b5e1-128">System.String</span></span>

## <span data-ttu-id="8b5e1-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b5e1-129">OUTPUTS</span></span>

### <span data-ttu-id="8b5e1-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8b5e1-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="8b5e1-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b5e1-131">NOTES</span></span>

## <span data-ttu-id="8b5e1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b5e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b5e1-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8b5e1-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="8b5e1-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8b5e1-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


