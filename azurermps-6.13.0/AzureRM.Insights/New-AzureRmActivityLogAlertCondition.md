---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 3904be513baf73c67c2dbd0018ae6b3e7e2226fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545252"
---
# <span data-ttu-id="ff53f-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ff53f-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="ff53f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff53f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff53f-103">Umożliwia utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ff53f-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff53f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff53f-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff53f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ff53f-105">DESCRIPTION</span></span>
<span data-ttu-id="ff53f-106">Polecenie cmdlet **New-AzureRmActivityLogAlertCondition** powoduje utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ff53f-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="ff53f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff53f-107">EXAMPLES</span></span>

### <span data-ttu-id="ff53f-108">Przykład 1: Tworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ff53f-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="ff53f-109">To polecenie tworzy nowy obiekt warunkowy alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ff53f-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="ff53f-110">**Uwaga** : Jeśli to polecenie cmdlet jest używane z Set-AzureRmActivityLogAlert co najmniej jeden z tych obiektów przekazanych jako parametry, musi mieć pole równe "Kategoria".</span><span class="sxs-lookup"><span data-stu-id="ff53f-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="ff53f-111">W przeciwnym razie wewnętrzna baza danych odpowie na 400 (BadRequest).</span><span class="sxs-lookup"><span data-stu-id="ff53f-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="ff53f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff53f-112">PARAMETERS</span></span>

### <span data-ttu-id="ff53f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff53f-113">-DefaultProfile</span></span>
<span data-ttu-id="ff53f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ff53f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff53f-115">-Równa się</span><span class="sxs-lookup"><span data-stu-id="ff53f-115">-Equal</span></span>
<span data-ttu-id="ff53f-116">Określa właściwość równości dla warunku typu liść.</span><span class="sxs-lookup"><span data-stu-id="ff53f-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="ff53f-117">-Pole</span><span class="sxs-lookup"><span data-stu-id="ff53f-117">-Field</span></span>
<span data-ttu-id="ff53f-118">Określa pole warunku.</span><span class="sxs-lookup"><span data-stu-id="ff53f-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="ff53f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff53f-119">CommonParameters</span></span>
<span data-ttu-id="ff53f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff53f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff53f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff53f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff53f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff53f-122">INPUTS</span></span>

### <span data-ttu-id="ff53f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ff53f-123">System.String</span></span>

## <span data-ttu-id="ff53f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff53f-124">OUTPUTS</span></span>

### <span data-ttu-id="ff53f-125">Microsoft. Azure. Management. Monitor. Management. models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="ff53f-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="ff53f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff53f-126">NOTES</span></span>

## <span data-ttu-id="ff53f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff53f-127">RELATED LINKS</span></span>

[<span data-ttu-id="ff53f-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ff53f-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ff53f-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ff53f-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ff53f-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ff53f-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ff53f-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ff53f-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ff53f-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ff53f-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ff53f-133">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="ff53f-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
