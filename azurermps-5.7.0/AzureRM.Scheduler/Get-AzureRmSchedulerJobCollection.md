---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718465"
---
# <span data-ttu-id="85dde-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="85dde-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="85dde-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85dde-102">SYNOPSIS</span></span>
<span data-ttu-id="85dde-103">Pobiera kolekcje zadań.</span><span class="sxs-lookup"><span data-stu-id="85dde-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85dde-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85dde-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85dde-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85dde-105">DESCRIPTION</span></span>
<span data-ttu-id="85dde-106">Polecenie cmdlet **Get-AzureRmSchedulerJobCollection** pobiera kolekcje zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="85dde-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="85dde-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85dde-107">EXAMPLES</span></span>

## <span data-ttu-id="85dde-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85dde-108">PARAMETERS</span></span>

### <span data-ttu-id="85dde-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dde-109">-DefaultProfile</span></span>
<span data-ttu-id="85dde-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85dde-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85dde-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="85dde-111">-JobCollectionName</span></span>
<span data-ttu-id="85dde-112">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="85dde-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dde-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85dde-113">-ResourceGroupName</span></span>
<span data-ttu-id="85dde-114">Określa grupę zasobów, z której to polecenie cmdlet pobiera kolekcje zadań.</span><span class="sxs-lookup"><span data-stu-id="85dde-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dde-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dde-115">CommonParameters</span></span>
<span data-ttu-id="85dde-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85dde-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dde-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85dde-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dde-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85dde-118">INPUTS</span></span>

### <span data-ttu-id="85dde-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85dde-119">None</span></span>
<span data-ttu-id="85dde-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="85dde-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85dde-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85dde-121">OUTPUTS</span></span>

### <span data-ttu-id="85dde-122">System. Object</span><span class="sxs-lookup"><span data-stu-id="85dde-122">System.Object</span></span>

## <span data-ttu-id="85dde-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85dde-123">NOTES</span></span>

## <span data-ttu-id="85dde-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85dde-124">RELATED LINKS</span></span>

[<span data-ttu-id="85dde-125">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="85dde-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="85dde-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="85dde-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="85dde-127">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="85dde-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="85dde-128">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="85dde-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="85dde-129">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="85dde-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


