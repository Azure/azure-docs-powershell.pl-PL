---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
ms.openlocfilehash: a7ad8616bf2afc79d049384c1f20002ff6d6aa4a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897442"
---
# <span data-ttu-id="482be-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="482be-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="482be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="482be-102">SYNOPSIS</span></span>
<span data-ttu-id="482be-103">Umożliwia utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="482be-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="482be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="482be-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="482be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="482be-105">DESCRIPTION</span></span>
<span data-ttu-id="482be-106">Polecenie cmdlet **New-AzureRmActivityLogAlertCondition** powoduje utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="482be-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="482be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="482be-107">EXAMPLES</span></span>

### <span data-ttu-id="482be-108">Przykład 1: Tworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="482be-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="482be-109">To polecenie tworzy nowy obiekt warunkowy alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="482be-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="482be-110">**Uwaga** : Jeśli to polecenie cmdlet jest używane z Set-AzureRmActivityLogAlert co najmniej jeden z tych obiektów przekazanych jako parametry, musi mieć pole równe "Kategoria".</span><span class="sxs-lookup"><span data-stu-id="482be-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="482be-111">W przeciwnym razie wewnętrzna baza danych odpowie na 400 (BadRequest).</span><span class="sxs-lookup"><span data-stu-id="482be-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="482be-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="482be-112">PARAMETERS</span></span>

### <span data-ttu-id="482be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482be-113">-DefaultProfile</span></span>
<span data-ttu-id="482be-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="482be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="482be-115">-Równa się</span><span class="sxs-lookup"><span data-stu-id="482be-115">-Equal</span></span>
<span data-ttu-id="482be-116">Określa właściwość równości dla warunku typu liść.</span><span class="sxs-lookup"><span data-stu-id="482be-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482be-117">-Pole</span><span class="sxs-lookup"><span data-stu-id="482be-117">-Field</span></span>
<span data-ttu-id="482be-118">Określa pole warunku.</span><span class="sxs-lookup"><span data-stu-id="482be-118">Specifies the field for the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482be-119">CommonParameters</span></span>
<span data-ttu-id="482be-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="482be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482be-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="482be-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482be-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="482be-122">INPUTS</span></span>

### <span data-ttu-id="482be-123">System. String</span><span class="sxs-lookup"><span data-stu-id="482be-123">System.String</span></span>

## <span data-ttu-id="482be-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="482be-124">OUTPUTS</span></span>

### <span data-ttu-id="482be-125">Microsoft. Azure. Management. Monitor. Management. models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="482be-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="482be-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="482be-126">NOTES</span></span>

## <span data-ttu-id="482be-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="482be-127">RELATED LINKS</span></span>

[<span data-ttu-id="482be-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="482be-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="482be-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="482be-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="482be-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="482be-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="482be-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="482be-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="482be-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="482be-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="482be-133">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="482be-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
