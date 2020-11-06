---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525826"
---
# <span data-ttu-id="b8291-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8291-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="b8291-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8291-102">SYNOPSIS</span></span>
<span data-ttu-id="b8291-103">Wznawia działanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b8291-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8291-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8291-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8291-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8291-105">DESCRIPTION</span></span>
<span data-ttu-id="b8291-106">Polecenie cmdlet Resume-AzureRmAnalysisServicesServer wznawia działanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b8291-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="b8291-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8291-107">EXAMPLES</span></span>

### <span data-ttu-id="b8291-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8291-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="b8291-109">To polecenie spowoduje wznowienie wstrzymanego serwera o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8291-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="b8291-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8291-110">PARAMETERS</span></span>

### <span data-ttu-id="b8291-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8291-111">-Name</span></span>
<span data-ttu-id="b8291-112">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b8291-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b8291-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8291-113">-PassThru</span></span>
<span data-ttu-id="b8291-114">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="b8291-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="b8291-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8291-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8291-116">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="b8291-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="b8291-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8291-117">-Confirm</span></span>
<span data-ttu-id="b8291-118">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="b8291-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="b8291-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8291-119">-WhatIf</span></span>
<span data-ttu-id="b8291-120">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="b8291-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="b8291-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8291-121">CommonParameters</span></span>
<span data-ttu-id="b8291-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8291-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8291-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8291-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8291-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8291-124">INPUTS</span></span>

## <span data-ttu-id="b8291-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8291-125">OUTPUTS</span></span>

### <span data-ttu-id="b8291-126">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8291-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="b8291-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8291-127">NOTES</span></span>
<span data-ttu-id="b8291-128">Alias: Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="b8291-128">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="b8291-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8291-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8291-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8291-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="b8291-131">Suspend — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b8291-131">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
