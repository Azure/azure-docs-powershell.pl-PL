---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 6abc37d37bf06025389329b8b917db8a75cefd1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990312"
---
# <span data-ttu-id="b198f-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b198f-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b198f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b198f-102">SYNOPSIS</span></span>
<span data-ttu-id="b198f-103">Tworzy nowego użytkownika dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="b198f-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="b198f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b198f-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b198f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b198f-105">DESCRIPTION</span></span>
<span data-ttu-id="b198f-106">Polecenie **cmdlet New-AzDataBoxEdgeUser** tworzy nowego użytkownika dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="b198f-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="b198f-107">Obsługiwane jest tworzenie tylko użytkowników `Share` tego typu.</span><span class="sxs-lookup"><span data-stu-id="b198f-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="b198f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b198f-108">EXAMPLES</span></span>

### <span data-ttu-id="b198f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b198f-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="b198f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b198f-110">PARAMETERS</span></span>

### <span data-ttu-id="b198f-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b198f-111">-AsJob</span></span>
<span data-ttu-id="b198f-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b198f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b198f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b198f-113">-DefaultProfile</span></span>
<span data-ttu-id="b198f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b198f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b198f-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b198f-115">-DeviceName</span></span>
<span data-ttu-id="b198f-116">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b198f-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-117">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="b198f-117">-EncryptionKey</span></span>
<span data-ttu-id="b198f-118">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="b198f-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="b198f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b198f-119">-Name</span></span>
<span data-ttu-id="b198f-120">Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="b198f-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-121">— Hasło</span><span class="sxs-lookup"><span data-stu-id="b198f-121">-Password</span></span>
<span data-ttu-id="b198f-122">Hasło, podaj jako bezpieczny ciąg</span><span class="sxs-lookup"><span data-stu-id="b198f-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="b198f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b198f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b198f-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b198f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b198f-125">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="b198f-125">-Type</span></span>
<span data-ttu-id="b198f-126">Wybierz pozycję UserType (Typ użytkownika)</span><span class="sxs-lookup"><span data-stu-id="b198f-126">Select UserType</span></span>

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

### <span data-ttu-id="b198f-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b198f-127">-Confirm</span></span>
<span data-ttu-id="b198f-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b198f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b198f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b198f-129">-WhatIf</span></span>
<span data-ttu-id="b198f-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b198f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b198f-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b198f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b198f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b198f-132">CommonParameters</span></span>
<span data-ttu-id="b198f-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b198f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b198f-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b198f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b198f-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b198f-135">INPUTS</span></span>

### <span data-ttu-id="b198f-136">Brak</span><span class="sxs-lookup"><span data-stu-id="b198f-136">None</span></span>

## <span data-ttu-id="b198f-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b198f-137">OUTPUTS</span></span>

### <span data-ttu-id="b198f-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b198f-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b198f-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b198f-139">NOTES</span></span>

## <span data-ttu-id="b198f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b198f-140">RELATED LINKS</span></span>
