---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242331"
---
# <span data-ttu-id="d8473-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="d8473-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="d8473-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8473-102">SYNOPSIS</span></span>
<span data-ttu-id="d8473-103">Usuwa kontakt zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="d8473-103">Deletes a security contact.</span></span>

## <span data-ttu-id="d8473-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8473-104">SYNTAX</span></span>

### <span data-ttu-id="d8473-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8473-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8473-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8473-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8473-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8473-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8473-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8473-108">DESCRIPTION</span></span>
<span data-ttu-id="d8473-109">Usuwa kontakt zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="d8473-109">Deletes a security contact.</span></span>

## <span data-ttu-id="d8473-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8473-110">EXAMPLES</span></span>

### <span data-ttu-id="d8473-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8473-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="d8473-112">Usuwa kontakt zabezpieczeń "default1"</span><span class="sxs-lookup"><span data-stu-id="d8473-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="d8473-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8473-113">PARAMETERS</span></span>

### <span data-ttu-id="d8473-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8473-114">-DefaultProfile</span></span>
<span data-ttu-id="d8473-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8473-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8473-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8473-116">-InputObject</span></span>
<span data-ttu-id="d8473-117">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="d8473-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8473-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8473-118">-Name</span></span>
<span data-ttu-id="d8473-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8473-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8473-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8473-120">-PassThru</span></span>
<span data-ttu-id="d8473-121">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="d8473-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d8473-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8473-122">-ResourceId</span></span>
<span data-ttu-id="d8473-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8473-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8473-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8473-124">-Confirm</span></span>
<span data-ttu-id="d8473-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8473-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8473-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8473-126">-WhatIf</span></span>
<span data-ttu-id="d8473-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8473-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8473-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8473-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8473-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8473-129">CommonParameters</span></span>
<span data-ttu-id="d8473-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8473-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8473-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8473-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8473-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8473-132">INPUTS</span></span>

### <span data-ttu-id="d8473-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d8473-133">System.String</span></span>

### <span data-ttu-id="d8473-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="d8473-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="d8473-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8473-135">OUTPUTS</span></span>

### <span data-ttu-id="d8473-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8473-136">System.Boolean</span></span>

## <span data-ttu-id="d8473-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8473-137">NOTES</span></span>

## <span data-ttu-id="d8473-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8473-138">RELATED LINKS</span></span>
