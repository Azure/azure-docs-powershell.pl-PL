---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 56cf34fce43465594a0a8862194bb15b117dda6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525069"
---
# <span data-ttu-id="2cc47-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2cc47-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="2cc47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cc47-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc47-103">Tworzy kolekcję obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="2cc47-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cc47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cc47-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cc47-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2cc47-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc47-106">Polecenie cmdlet **New-AzureRmPowerBIWorkspaceCollection** tworzy kolekcję obszarów roboczych usługi Power BI dla subskrypcji platformy Azure w określonej grupie zasobów i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2cc47-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="2cc47-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cc47-107">EXAMPLES</span></span>

### <span data-ttu-id="2cc47-108">Przykład 1. Tworzenie kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="2cc47-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="2cc47-109">To polecenie tworzy kolekcję obszarów roboczych o nazwie WCN11 w określonej lokalizacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2cc47-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="2cc47-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cc47-110">PARAMETERS</span></span>

### <span data-ttu-id="2cc47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc47-111">-DefaultProfile</span></span>
<span data-ttu-id="2cc47-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2cc47-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cc47-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2cc47-113">-Location</span></span>
<span data-ttu-id="2cc47-114">Określa lokalizację platformy Azure, w której to polecenie cmdlet tworzy kolekcję obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="2cc47-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc47-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc47-115">-ResourceGroupName</span></span>
<span data-ttu-id="2cc47-116">Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy kolekcję obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="2cc47-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="2cc47-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="2cc47-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="2cc47-118">Określa nazwę kolekcji obszaru roboczego usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="2cc47-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="2cc47-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2cc47-119">-Confirm</span></span>
<span data-ttu-id="2cc47-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cc47-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc47-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc47-121">-WhatIf</span></span>
<span data-ttu-id="2cc47-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cc47-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cc47-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2cc47-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc47-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc47-124">CommonParameters</span></span>
<span data-ttu-id="2cc47-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc47-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc47-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc47-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc47-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cc47-127">INPUTS</span></span>

### <span data-ttu-id="2cc47-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2cc47-128">None</span></span>
<span data-ttu-id="2cc47-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2cc47-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2cc47-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cc47-130">OUTPUTS</span></span>

### <span data-ttu-id="2cc47-131">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2cc47-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="2cc47-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cc47-132">NOTES</span></span>

## <span data-ttu-id="2cc47-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cc47-133">RELATED LINKS</span></span>

[<span data-ttu-id="2cc47-134">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2cc47-134">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="2cc47-135">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="2cc47-135">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


