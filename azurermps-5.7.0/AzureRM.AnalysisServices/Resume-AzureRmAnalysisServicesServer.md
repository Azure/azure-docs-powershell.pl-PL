---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 5d3d2c4d630ccb31d3d59a610881aa92a4e8b844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717759"
---
# <span data-ttu-id="90c90-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="90c90-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="90c90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90c90-102">SYNOPSIS</span></span>
<span data-ttu-id="90c90-103">Wznawia działanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="90c90-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90c90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90c90-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90c90-105">DESCRIPTION</span></span>
<span data-ttu-id="90c90-106">Polecenie cmdlet Resume-AzureRmAnalysisServicesServer wznawia działanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="90c90-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="90c90-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90c90-107">EXAMPLES</span></span>

### <span data-ttu-id="90c90-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90c90-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="90c90-109">To polecenie spowoduje wznowienie wstrzymanego serwera o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="90c90-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="90c90-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90c90-110">PARAMETERS</span></span>

### <span data-ttu-id="90c90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c90-111">-DefaultProfile</span></span>
<span data-ttu-id="90c90-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90c90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c90-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90c90-113">-Name</span></span>
<span data-ttu-id="90c90-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="90c90-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="90c90-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90c90-115">-PassThru</span></span>
<span data-ttu-id="90c90-116">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="90c90-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="90c90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c90-117">-ResourceGroupName</span></span>
<span data-ttu-id="90c90-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="90c90-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="90c90-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90c90-119">-Confirm</span></span>
<span data-ttu-id="90c90-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="90c90-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="90c90-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c90-121">-WhatIf</span></span>
<span data-ttu-id="90c90-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="90c90-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="90c90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c90-123">CommonParameters</span></span>
<span data-ttu-id="90c90-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c90-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c90-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c90-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90c90-126">INPUTS</span></span>

### <span data-ttu-id="90c90-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90c90-127">None</span></span>
<span data-ttu-id="90c90-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="90c90-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90c90-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90c90-129">OUTPUTS</span></span>

### <span data-ttu-id="90c90-130">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="90c90-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="90c90-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90c90-131">NOTES</span></span>
<span data-ttu-id="90c90-132">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="90c90-132">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="90c90-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90c90-133">RELATED LINKS</span></span>

[<span data-ttu-id="90c90-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="90c90-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="90c90-135">Suspend — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="90c90-135">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
