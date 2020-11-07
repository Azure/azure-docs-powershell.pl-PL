---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7f3a48db5d8f1e6c7b4b0e73b705fc375a0b514f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718489"
---
# <span data-ttu-id="6cafe-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6cafe-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="6cafe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cafe-102">SYNOPSIS</span></span>
<span data-ttu-id="6cafe-103">Usuwa kolekcję obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="6cafe-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cafe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cafe-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cafe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6cafe-105">DESCRIPTION</span></span>
<span data-ttu-id="6cafe-106">Polecenie cmdlet **Remove-AzureRmPowerBIWorkspaceCollection** usuwa kolekcję obszarów roboczych usługi Power BI z subskrypcji i grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6cafe-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="6cafe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cafe-107">EXAMPLES</span></span>

### <span data-ttu-id="6cafe-108">Przykład 1: usuwanie kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="6cafe-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="6cafe-109">To polecenie usuwa kolekcję obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6cafe-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="6cafe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cafe-110">PARAMETERS</span></span>

### <span data-ttu-id="6cafe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cafe-111">-DefaultProfile</span></span>
<span data-ttu-id="6cafe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6cafe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cafe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cafe-113">-ResourceGroupName</span></span>
<span data-ttu-id="6cafe-114">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa kolekcję obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="6cafe-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cafe-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="6cafe-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="6cafe-116">Określa nazwę kolekcji obszaru roboczego usługi Power BI, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cafe-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cafe-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6cafe-117">-Confirm</span></span>
<span data-ttu-id="6cafe-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cafe-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cafe-119">-WhatIf</span></span>
<span data-ttu-id="6cafe-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cafe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cafe-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6cafe-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cafe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cafe-122">CommonParameters</span></span>
<span data-ttu-id="6cafe-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cafe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cafe-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cafe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cafe-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cafe-125">INPUTS</span></span>

### <span data-ttu-id="6cafe-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6cafe-126">None</span></span>
<span data-ttu-id="6cafe-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6cafe-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6cafe-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cafe-128">OUTPUTS</span></span>

## <span data-ttu-id="6cafe-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cafe-129">NOTES</span></span>

## <span data-ttu-id="6cafe-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cafe-130">RELATED LINKS</span></span>

[<span data-ttu-id="6cafe-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6cafe-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="6cafe-132">Nowe — AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6cafe-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


