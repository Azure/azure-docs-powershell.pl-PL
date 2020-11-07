---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 23dd49b6c331f29111c6e203517d815ee6b24b53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870424"
---
# <span data-ttu-id="4d390-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4d390-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="4d390-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d390-102">SYNOPSIS</span></span>
<span data-ttu-id="4d390-103">Umożliwia utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4d390-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="4d390-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d390-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d390-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d390-105">DESCRIPTION</span></span>
<span data-ttu-id="4d390-106">Polecenie cmdlet **New-AzActivityLogAlertCondition** powoduje utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4d390-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="4d390-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d390-107">EXAMPLES</span></span>

### <span data-ttu-id="4d390-108">Przykład 1: Tworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4d390-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="4d390-109">To polecenie tworzy nowy obiekt warunkowy alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4d390-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="4d390-110">**Uwaga** : Jeśli to polecenie cmdlet jest używane z Set-AzActivityLogAlert co najmniej jeden z tych obiektów przekazanych jako parametry, musi mieć pole równe "Kategoria".</span><span class="sxs-lookup"><span data-stu-id="4d390-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="4d390-111">W przeciwnym razie wewnętrzna baza danych odpowie na 400 (BadRequest).</span><span class="sxs-lookup"><span data-stu-id="4d390-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="4d390-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d390-112">PARAMETERS</span></span>

### <span data-ttu-id="4d390-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d390-113">-DefaultProfile</span></span>
<span data-ttu-id="4d390-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4d390-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d390-115">-Równa się</span><span class="sxs-lookup"><span data-stu-id="4d390-115">-Equal</span></span>
<span data-ttu-id="4d390-116">Określa właściwość równości dla warunku typu liść.</span><span class="sxs-lookup"><span data-stu-id="4d390-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="4d390-117">-Pole</span><span class="sxs-lookup"><span data-stu-id="4d390-117">-Field</span></span>
<span data-ttu-id="4d390-118">Określa pole warunku.</span><span class="sxs-lookup"><span data-stu-id="4d390-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="4d390-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d390-119">CommonParameters</span></span>
<span data-ttu-id="4d390-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d390-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d390-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d390-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d390-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d390-122">INPUTS</span></span>

### <span data-ttu-id="4d390-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4d390-123">System.String</span></span>

## <span data-ttu-id="4d390-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d390-124">OUTPUTS</span></span>

### <span data-ttu-id="4d390-125">Microsoft. Azure. Management. Monitor. Management. models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="4d390-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="4d390-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d390-126">NOTES</span></span>

## <span data-ttu-id="4d390-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d390-127">RELATED LINKS</span></span>

[<span data-ttu-id="4d390-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d390-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="4d390-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d390-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="4d390-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d390-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="4d390-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d390-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="4d390-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d390-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="4d390-133">Nowe — AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="4d390-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
