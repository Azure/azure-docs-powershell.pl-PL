---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 116dfd9d38325682e6a80361b40bc8dd84b133fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528161"
---
# <span data-ttu-id="218d9-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="218d9-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="218d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="218d9-102">SYNOPSIS</span></span>
<span data-ttu-id="218d9-103">Wstrzymuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="218d9-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="218d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="218d9-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="218d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="218d9-105">DESCRIPTION</span></span>
<span data-ttu-id="218d9-106">Polecenie Suspend-AzureRmAnalysisServicesServer polecenia zawiesza wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="218d9-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="218d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="218d9-107">EXAMPLES</span></span>

### <span data-ttu-id="218d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="218d9-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="218d9-109">To polecenie spowoduje zawieszenie aktywnego serwera o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="218d9-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="218d9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="218d9-110">PARAMETERS</span></span>

### <span data-ttu-id="218d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218d9-111">-DefaultProfile</span></span>
<span data-ttu-id="218d9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="218d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="218d9-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="218d9-113">-Name</span></span>
<span data-ttu-id="218d9-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="218d9-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="218d9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="218d9-115">-PassThru</span></span>
<span data-ttu-id="218d9-116">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="218d9-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="218d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="218d9-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="218d9-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="218d9-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="218d9-119">-Confirm</span></span>
<span data-ttu-id="218d9-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="218d9-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="218d9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218d9-121">-WhatIf</span></span>
<span data-ttu-id="218d9-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="218d9-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="218d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218d9-123">CommonParameters</span></span>
<span data-ttu-id="218d9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="218d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218d9-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="218d9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218d9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="218d9-126">INPUTS</span></span>

### <span data-ttu-id="218d9-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="218d9-127">None</span></span>
<span data-ttu-id="218d9-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="218d9-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="218d9-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="218d9-129">OUTPUTS</span></span>

### <span data-ttu-id="218d9-130">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="218d9-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="218d9-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="218d9-131">NOTES</span></span>
<span data-ttu-id="218d9-132">Alias: Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="218d9-132">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="218d9-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="218d9-133">RELATED LINKS</span></span>

[<span data-ttu-id="218d9-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="218d9-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="218d9-135">Życiorys — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="218d9-135">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)
