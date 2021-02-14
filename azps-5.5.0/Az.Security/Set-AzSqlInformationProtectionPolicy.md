---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201786"
---
# <span data-ttu-id="c3bf8-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3bf8-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="c3bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="c3bf8-103">Ustawia skuteczne zasady ochrony informacji SQL dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="c3bf8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3bf8-104">SYNTAX</span></span>

### <span data-ttu-id="c3bf8-105">Zasady ochrony informacji SQL (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c3bf8-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3bf8-106">Ścieżka pliku zasad SQL Information Protection Policy</span><span class="sxs-lookup"><span data-stu-id="c3bf8-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3bf8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3bf8-107">DESCRIPTION</span></span>
<span data-ttu-id="c3bf8-108">Ustawia skuteczne zasady ochrony informacji SQL dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="c3bf8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3bf8-109">EXAMPLES</span></span>

### <span data-ttu-id="c3bf8-110">Przykład</span><span class="sxs-lookup"><span data-stu-id="c3bf8-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="c3bf8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3bf8-111">PARAMETERS</span></span>

### <span data-ttu-id="c3bf8-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c3bf8-112">-AsJob</span></span>
<span data-ttu-id="c3bf8-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c3bf8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3bf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3bf8-114">-DefaultProfile</span></span>
<span data-ttu-id="c3bf8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3bf8-116">- FilePath</span><span class="sxs-lookup"><span data-stu-id="c3bf8-116">-FilePath</span></span>
<span data-ttu-id="c3bf8-117">Określa ścieżkę pliku json zawierającego definicję zasad ochrony informacji SQL.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3bf8-118">— Zasady</span><span class="sxs-lookup"><span data-stu-id="c3bf8-118">-Policy</span></span>
<span data-ttu-id="c3bf8-119">Określa definicję zasad ochrony informacji SQL.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="c3bf8-120">Można określić ścieżkę pliku json lub ciąg formatu JSON definiujący zasady.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3bf8-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3bf8-121">-Confirm</span></span>
<span data-ttu-id="c3bf8-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3bf8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3bf8-123">-WhatIf</span></span>
<span data-ttu-id="c3bf8-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3bf8-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3bf8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3bf8-126">CommonParameters</span></span>
<span data-ttu-id="c3bf8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3bf8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3bf8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3bf8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3bf8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3bf8-129">INPUTS</span></span>

### <span data-ttu-id="c3bf8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c3bf8-130">System.String</span></span>

## <span data-ttu-id="c3bf8-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3bf8-131">OUTPUTS</span></span>

### <span data-ttu-id="c3bf8-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3bf8-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="c3bf8-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3bf8-133">NOTES</span></span>

## <span data-ttu-id="c3bf8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3bf8-134">RELATED LINKS</span></span>
