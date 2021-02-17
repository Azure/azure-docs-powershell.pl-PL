---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198723"
---
# <span data-ttu-id="60a0f-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60a0f-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="60a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="60a0f-103">Pobiera efektywne zasady ochrony informacji SQL dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="60a0f-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="60a0f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="60a0f-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a0f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="60a0f-105">DESCRIPTION</span></span>
<span data-ttu-id="60a0f-106">Pobiera efektywne zasady ochrony informacji SQL dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="60a0f-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="60a0f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="60a0f-107">EXAMPLES</span></span>

### <span data-ttu-id="60a0f-108">Przykład</span><span class="sxs-lookup"><span data-stu-id="60a0f-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="60a0f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60a0f-109">PARAMETERS</span></span>

### <span data-ttu-id="60a0f-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="60a0f-110">-AsJob</span></span>
<span data-ttu-id="60a0f-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="60a0f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60a0f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a0f-112">-DefaultProfile</span></span>
<span data-ttu-id="60a0f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="60a0f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a0f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a0f-114">CommonParameters</span></span>
<span data-ttu-id="60a0f-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a0f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a0f-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60a0f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a0f-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60a0f-117">INPUTS</span></span>

### <span data-ttu-id="60a0f-118">System.string</span><span class="sxs-lookup"><span data-stu-id="60a0f-118">System.string</span></span>

## <span data-ttu-id="60a0f-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60a0f-119">OUTPUTS</span></span>

### <span data-ttu-id="60a0f-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60a0f-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="60a0f-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="60a0f-121">NOTES</span></span>

## <span data-ttu-id="60a0f-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60a0f-122">RELATED LINKS</span></span>
