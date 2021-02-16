---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185131"
---
# <span data-ttu-id="4fd5a-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4fd5a-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="4fd5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd5a-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd5a-103">Usuń identyfikator MPN (Microsoft Partner Network) bieżącego uwierzytelnionego użytkownika lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="4fd5a-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="4fd5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4fd5a-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd5a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4fd5a-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd5a-106">Usuń identyfikator MPN (Microsoft Partner Network) bieżącego uwierzytelnionego użytkownika lub podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="4fd5a-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="4fd5a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4fd5a-107">EXAMPLES</span></span>

### <span data-ttu-id="4fd5a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4fd5a-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="4fd5a-109">Usuwanie partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="4fd5a-109">Remove management partner</span></span>

## <span data-ttu-id="4fd5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fd5a-110">PARAMETERS</span></span>

### <span data-ttu-id="4fd5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd5a-111">-DefaultProfile</span></span>
<span data-ttu-id="4fd5a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd5a-113">- PartnerId</span><span class="sxs-lookup"><span data-stu-id="4fd5a-113">-PartnerId</span></span>
<span data-ttu-id="4fd5a-114">Identyfikator partnera zarządzania to 6-cyfrowy numer</span><span class="sxs-lookup"><span data-stu-id="4fd5a-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="4fd5a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fd5a-115">-PassThru</span></span>
<span data-ttu-id="4fd5a-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4fd5a-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4fd5a-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4fd5a-117">-Confirm</span></span>
<span data-ttu-id="4fd5a-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4fd5a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd5a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd5a-119">-WhatIf</span></span>
<span data-ttu-id="4fd5a-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd5a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd5a-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4fd5a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd5a-122">CommonParameters</span></span>
<span data-ttu-id="4fd5a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd5a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd5a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd5a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fd5a-125">INPUTS</span></span>

### <span data-ttu-id="4fd5a-126">Brak</span><span class="sxs-lookup"><span data-stu-id="4fd5a-126">None</span></span>

## <span data-ttu-id="4fd5a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fd5a-127">OUTPUTS</span></span>

### <span data-ttu-id="4fd5a-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fd5a-128">System.Boolean</span></span>

## <span data-ttu-id="4fd5a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4fd5a-129">NOTES</span></span>

## <span data-ttu-id="4fd5a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fd5a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4fd5a-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4fd5a-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="4fd5a-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4fd5a-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="4fd5a-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4fd5a-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)