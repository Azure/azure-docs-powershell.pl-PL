---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503030"
---
# <span data-ttu-id="701a2-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="701a2-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="701a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="701a2-102">SYNOPSIS</span></span>
<span data-ttu-id="701a2-103">Pobiera efektywne zasady ochrony danych usługi SQL dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="701a2-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="701a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="701a2-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="701a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="701a2-105">DESCRIPTION</span></span>
<span data-ttu-id="701a2-106">Pobiera efektywne zasady ochrony danych usługi SQL dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="701a2-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="701a2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="701a2-107">EXAMPLES</span></span>

### <span data-ttu-id="701a2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="701a2-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="701a2-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="701a2-109">PARAMETERS</span></span>

### <span data-ttu-id="701a2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="701a2-110">-AsJob</span></span>
<span data-ttu-id="701a2-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="701a2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="701a2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="701a2-112">-DefaultProfile</span></span>
<span data-ttu-id="701a2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="701a2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="701a2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="701a2-114">CommonParameters</span></span>
<span data-ttu-id="701a2-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="701a2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="701a2-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="701a2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="701a2-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="701a2-117">INPUTS</span></span>

### <span data-ttu-id="701a2-118">System. String</span><span class="sxs-lookup"><span data-stu-id="701a2-118">System.string</span></span>

## <span data-ttu-id="701a2-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="701a2-119">OUTPUTS</span></span>

### <span data-ttu-id="701a2-120">Microsoft. Azure. Commands. SecurityCenter. modele. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="701a2-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="701a2-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="701a2-121">NOTES</span></span>

## <span data-ttu-id="701a2-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="701a2-122">RELATED LINKS</span></span>
