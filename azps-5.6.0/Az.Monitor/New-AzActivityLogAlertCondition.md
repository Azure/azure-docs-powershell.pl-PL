---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: f18479f8cf42c68a7c8a8a5d9f45a4542a758212
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979898"
---
# <span data-ttu-id="04497-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="04497-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="04497-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04497-102">SYNOPSIS</span></span>
<span data-ttu-id="04497-103">Tworzy w pamięci nowy obiekt warunku alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="04497-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="04497-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04497-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04497-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="04497-105">DESCRIPTION</span></span>
<span data-ttu-id="04497-106">Polecenie **cmdlet New-AzActivityLogAlertCondition** tworzy w pamięci nowy obiekt warunku dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="04497-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="04497-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04497-107">EXAMPLES</span></span>

### <span data-ttu-id="04497-108">Przykład 1. Tworzenie nowego obiektu alertu dziennika aktywności w pamięci.</span><span class="sxs-lookup"><span data-stu-id="04497-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="04497-109">To polecenie tworzy w pamięci nowy obiekt warunku alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="04497-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="04497-110">**UWAGA:** po użyciu tego polecenia cmdlet z parametrem [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) co najmniej jeden z tych obiektów przekazanych jako parametry musi mieć wartość "Category" (Kategoria).</span><span class="sxs-lookup"><span data-stu-id="04497-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="04497-111">W przeciwnym razie zareaguje na 400 (BadRequest).</span><span class="sxs-lookup"><span data-stu-id="04497-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="04497-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04497-112">PARAMETERS</span></span>

### <span data-ttu-id="04497-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04497-113">-DefaultProfile</span></span>
<span data-ttu-id="04497-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="04497-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04497-115">-Equal</span><span class="sxs-lookup"><span data-stu-id="04497-115">-Equal</span></span>
<span data-ttu-id="04497-116">Określa właściwość równa się dla warunku liścia.</span><span class="sxs-lookup"><span data-stu-id="04497-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="04497-117">- Pole</span><span class="sxs-lookup"><span data-stu-id="04497-117">-Field</span></span>
<span data-ttu-id="04497-118">Określa pole warunku.</span><span class="sxs-lookup"><span data-stu-id="04497-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="04497-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04497-119">CommonParameters</span></span>
<span data-ttu-id="04497-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04497-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04497-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04497-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04497-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04497-122">INPUTS</span></span>

### <span data-ttu-id="04497-123">System.String</span><span class="sxs-lookup"><span data-stu-id="04497-123">System.String</span></span>

## <span data-ttu-id="04497-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04497-124">OUTPUTS</span></span>

### <span data-ttu-id="04497-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="04497-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="04497-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04497-126">NOTES</span></span>

## <span data-ttu-id="04497-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04497-127">RELATED LINKS</span></span>

[<span data-ttu-id="04497-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04497-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="04497-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04497-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="04497-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04497-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="04497-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04497-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="04497-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="04497-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="04497-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="04497-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
