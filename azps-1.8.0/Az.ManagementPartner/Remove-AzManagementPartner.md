---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 5910d82ddee49ba47c709a3323f72e325f4067ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867460"
---
# <span data-ttu-id="7cab0-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7cab0-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="7cab0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cab0-102">SYNOPSIS</span></span>
<span data-ttu-id="7cab0-103">Usuń identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="7cab0-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="7cab0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cab0-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cab0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7cab0-105">DESCRIPTION</span></span>
<span data-ttu-id="7cab0-106">Usuń identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="7cab0-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="7cab0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cab0-107">EXAMPLES</span></span>

### <span data-ttu-id="7cab0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7cab0-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="7cab0-109">Usuń partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="7cab0-109">Remove management partner</span></span>

## <span data-ttu-id="7cab0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cab0-110">PARAMETERS</span></span>

### <span data-ttu-id="7cab0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cab0-111">-DefaultProfile</span></span>
<span data-ttu-id="7cab0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cab0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cab0-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="7cab0-113">-PartnerId</span></span>
<span data-ttu-id="7cab0-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="7cab0-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="7cab0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cab0-115">-PassThru</span></span>
<span data-ttu-id="7cab0-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7cab0-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cab0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cab0-117">-Confirm</span></span>
<span data-ttu-id="7cab0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cab0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cab0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cab0-119">-WhatIf</span></span>
<span data-ttu-id="7cab0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cab0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cab0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7cab0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cab0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cab0-122">CommonParameters</span></span>
<span data-ttu-id="7cab0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cab0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cab0-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cab0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cab0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cab0-125">INPUTS</span></span>

### <span data-ttu-id="7cab0-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7cab0-126">None</span></span>

## <span data-ttu-id="7cab0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cab0-127">OUTPUTS</span></span>

### <span data-ttu-id="7cab0-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cab0-128">System.Boolean</span></span>

## <span data-ttu-id="7cab0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cab0-129">NOTES</span></span>

## <span data-ttu-id="7cab0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cab0-130">RELATED LINKS</span></span>

[<span data-ttu-id="7cab0-131">Nowe — AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7cab0-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="7cab0-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7cab0-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="7cab0-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7cab0-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)