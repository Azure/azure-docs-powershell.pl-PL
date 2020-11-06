---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 35b8788c67098a45f6a5373e90b7a93fbcbc4703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525817"
---
# <span data-ttu-id="6acc6-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6acc6-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="6acc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6acc6-102">SYNOPSIS</span></span>
<span data-ttu-id="6acc6-103">Wstrzymuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6acc6-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6acc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6acc6-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6acc6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6acc6-105">DESCRIPTION</span></span>
<span data-ttu-id="6acc6-106">Polecenie Suspend-AzureRmAnalysisServicesServer polecenia zawiesza wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6acc6-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="6acc6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6acc6-107">EXAMPLES</span></span>

### <span data-ttu-id="6acc6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6acc6-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="6acc6-109">To polecenie spowoduje zawieszenie aktywnego serwera o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="6acc6-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="6acc6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6acc6-110">PARAMETERS</span></span>

### <span data-ttu-id="6acc6-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6acc6-111">-Name</span></span>
<span data-ttu-id="6acc6-112">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6acc6-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="6acc6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6acc6-113">-PassThru</span></span>
<span data-ttu-id="6acc6-114">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="6acc6-114">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6acc6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6acc6-115">-ResourceGroupName</span></span>
<span data-ttu-id="6acc6-116">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="6acc6-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6acc6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6acc6-117">-Confirm</span></span>
<span data-ttu-id="6acc6-118">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="6acc6-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="6acc6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6acc6-119">-WhatIf</span></span>
<span data-ttu-id="6acc6-120">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="6acc6-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="6acc6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6acc6-121">CommonParameters</span></span>
<span data-ttu-id="6acc6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6acc6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6acc6-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6acc6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6acc6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6acc6-124">INPUTS</span></span>

## <span data-ttu-id="6acc6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6acc6-125">OUTPUTS</span></span>

### <span data-ttu-id="6acc6-126">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6acc6-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="6acc6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6acc6-127">NOTES</span></span>
<span data-ttu-id="6acc6-128">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="6acc6-128">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="6acc6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6acc6-129">RELATED LINKS</span></span>

[<span data-ttu-id="6acc6-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6acc6-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="6acc6-131">Życiorys — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6acc6-131">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

