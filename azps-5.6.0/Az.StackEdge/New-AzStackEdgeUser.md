---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: cd904a913ce9ea0cdcc2d347463fa21ac7e13943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005210"
---
# <span data-ttu-id="ab201-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="ab201-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="ab201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab201-102">SYNOPSIS</span></span>
<span data-ttu-id="ab201-103">Tworzy nowego użytkownika dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="ab201-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="ab201-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab201-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab201-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab201-105">DESCRIPTION</span></span>
<span data-ttu-id="ab201-106">Polecenie **cmdlet New-AzStackEdgeUser** tworzy nowego użytkownika dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="ab201-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="ab201-107">Obsługiwane jest tworzenie tylko użytkowników `Share` tego typu.</span><span class="sxs-lookup"><span data-stu-id="ab201-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="ab201-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab201-108">EXAMPLES</span></span>

### <span data-ttu-id="ab201-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab201-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="ab201-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab201-110">PARAMETERS</span></span>

### <span data-ttu-id="ab201-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ab201-111">-AsJob</span></span>
<span data-ttu-id="ab201-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ab201-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab201-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab201-113">-DefaultProfile</span></span>
<span data-ttu-id="ab201-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab201-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab201-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ab201-115">-DeviceName</span></span>
<span data-ttu-id="ab201-116">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="ab201-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab201-117">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="ab201-117">-EncryptionKey</span></span>
<span data-ttu-id="ab201-118">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="ab201-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab201-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ab201-119">-Name</span></span>
<span data-ttu-id="ab201-120">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="ab201-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab201-121">— Hasło</span><span class="sxs-lookup"><span data-stu-id="ab201-121">-Password</span></span>
<span data-ttu-id="ab201-122">Hasło, podaj jako bezpieczny ciąg</span><span class="sxs-lookup"><span data-stu-id="ab201-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab201-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab201-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab201-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ab201-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab201-125">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="ab201-125">-Type</span></span>
<span data-ttu-id="ab201-126">Wybierz pozycję UserType (Typ użytkownika)</span><span class="sxs-lookup"><span data-stu-id="ab201-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab201-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab201-127">-Confirm</span></span>
<span data-ttu-id="ab201-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab201-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab201-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab201-129">-WhatIf</span></span>
<span data-ttu-id="ab201-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab201-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab201-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ab201-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab201-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab201-132">CommonParameters</span></span>
<span data-ttu-id="ab201-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab201-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab201-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab201-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab201-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab201-135">INPUTS</span></span>

### <span data-ttu-id="ab201-136">Brak</span><span class="sxs-lookup"><span data-stu-id="ab201-136">None</span></span>

## <span data-ttu-id="ab201-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab201-137">OUTPUTS</span></span>

### <span data-ttu-id="ab201-138">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ab201-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ab201-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab201-139">NOTES</span></span>

## <span data-ttu-id="ab201-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab201-140">RELATED LINKS</span></span>
