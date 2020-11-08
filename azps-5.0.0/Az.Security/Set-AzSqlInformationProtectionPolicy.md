---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225151"
---
# <span data-ttu-id="5050e-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5050e-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="5050e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5050e-102">SYNOPSIS</span></span>
<span data-ttu-id="5050e-103">Ustawia efektywne zasady ochrony danych usługi SQL dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5050e-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="5050e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5050e-104">SYNTAX</span></span>

### <span data-ttu-id="5050e-105">Zasady dotyczące ochrony danych SQL (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5050e-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5050e-106">Ścieżka pliku zasad ochrony danych SQL</span><span class="sxs-lookup"><span data-stu-id="5050e-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5050e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5050e-107">DESCRIPTION</span></span>
<span data-ttu-id="5050e-108">Ustawia efektywne zasady ochrony danych usługi SQL dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5050e-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="5050e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5050e-109">EXAMPLES</span></span>

### <span data-ttu-id="5050e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5050e-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="5050e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5050e-111">PARAMETERS</span></span>

### <span data-ttu-id="5050e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5050e-112">-AsJob</span></span>
<span data-ttu-id="5050e-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5050e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5050e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5050e-114">-DefaultProfile</span></span>
<span data-ttu-id="5050e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5050e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5050e-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5050e-116">-FilePath</span></span>
<span data-ttu-id="5050e-117">Określa ścieżkę pliku JSON zawierającego definicję zasad usługi SQL Information Protection.</span><span class="sxs-lookup"><span data-stu-id="5050e-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="5050e-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="5050e-118">-Policy</span></span>
<span data-ttu-id="5050e-119">Określa definicję zasad dotyczących ochrony danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5050e-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="5050e-120">Możesz określić ścieżkę pliku JSON lub ciąg formatu JSON definiujący zasady.</span><span class="sxs-lookup"><span data-stu-id="5050e-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="5050e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5050e-121">-Confirm</span></span>
<span data-ttu-id="5050e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5050e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5050e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5050e-123">-WhatIf</span></span>
<span data-ttu-id="5050e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5050e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5050e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5050e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5050e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5050e-126">CommonParameters</span></span>
<span data-ttu-id="5050e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5050e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5050e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5050e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5050e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5050e-129">INPUTS</span></span>

### <span data-ttu-id="5050e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5050e-130">System.String</span></span>

## <span data-ttu-id="5050e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5050e-131">OUTPUTS</span></span>

### <span data-ttu-id="5050e-132">Microsoft. Azure. Commands. SecurityCenter. modele. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5050e-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="5050e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5050e-133">NOTES</span></span>

## <span data-ttu-id="5050e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5050e-134">RELATED LINKS</span></span>
