---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 7329889dbc0484e8747b27d49b8781547dcfc256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704895"
---
# <span data-ttu-id="ad548-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ad548-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="ad548-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad548-102">SYNOPSIS</span></span>
<span data-ttu-id="ad548-103">Kojarzy identyfikator sieci partnera firmy Microsoft (MPN) z bieżącym użytkownikiem uwierzytelnionym lub usługą.</span><span class="sxs-lookup"><span data-stu-id="ad548-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="ad548-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad548-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad548-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad548-105">DESCRIPTION</span></span>
<span data-ttu-id="ad548-106">Kojarzy identyfikator sieci partnera firmy Microsoft (MPN) z bieżącym użytkownikiem uwierzytelnionym lub usługą.</span><span class="sxs-lookup"><span data-stu-id="ad548-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="ad548-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad548-107">EXAMPLES</span></span>

### <span data-ttu-id="ad548-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad548-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="ad548-109">Dodawanie partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="ad548-109">Add a management partner</span></span>

## <span data-ttu-id="ad548-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad548-110">PARAMETERS</span></span>

### <span data-ttu-id="ad548-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad548-111">-DefaultProfile</span></span>
<span data-ttu-id="ad548-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad548-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad548-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="ad548-113">-PartnerId</span></span>
<span data-ttu-id="ad548-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="ad548-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad548-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad548-115">-Confirm</span></span>
<span data-ttu-id="ad548-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad548-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad548-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad548-117">-WhatIf</span></span>
<span data-ttu-id="ad548-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad548-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad548-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad548-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad548-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad548-120">CommonParameters</span></span>
<span data-ttu-id="ad548-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad548-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad548-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad548-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad548-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad548-123">INPUTS</span></span>

### <span data-ttu-id="ad548-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ad548-124">None</span></span>

## <span data-ttu-id="ad548-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad548-125">OUTPUTS</span></span>

### <span data-ttu-id="ad548-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ad548-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="ad548-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad548-127">NOTES</span></span>

## <span data-ttu-id="ad548-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad548-128">RELATED LINKS</span></span>

[<span data-ttu-id="ad548-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ad548-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="ad548-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ad548-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="ad548-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ad548-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)