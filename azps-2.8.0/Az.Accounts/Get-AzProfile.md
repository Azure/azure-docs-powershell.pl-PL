---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 937683c8592bb814b7f6a6262ef095cbd8252c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707216"
---
# <span data-ttu-id="f8ca5-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="f8ca5-101">Get-AzProfile</span></span>

## <span data-ttu-id="f8ca5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ca5-103">Pobierz profile usług obsługiwane przez zainstalowane moduły.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f8ca5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8ca5-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="f8ca5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ca5-106">Pobierz profile usług obsługiwane przez zainstalowane moduły.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f8ca5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8ca5-107">EXAMPLES</span></span>

### <span data-ttu-id="f8ca5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f8ca5-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="f8ca5-109">Uzyskiwanie profilu usługi obsługiwanego przez moduł magazynu</span><span class="sxs-lookup"><span data-stu-id="f8ca5-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="f8ca5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8ca5-110">PARAMETERS</span></span>

### <span data-ttu-id="f8ca5-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f8ca5-111">-ListAvailable</span></span>
<span data-ttu-id="f8ca5-112">Lista wszystkich profilów usługi obsługiwanych przez zainstalowane moduły</span><span class="sxs-lookup"><span data-stu-id="f8ca5-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="f8ca5-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="f8ca5-113">-ModuleName</span></span>
<span data-ttu-id="f8ca5-114">Nazwa modułu do sprawdzenia</span><span class="sxs-lookup"><span data-stu-id="f8ca5-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ca5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ca5-115">CommonParameters</span></span>
<span data-ttu-id="f8ca5-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ca5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ca5-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ca5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ca5-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8ca5-118">INPUTS</span></span>

### <span data-ttu-id="f8ca5-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f8ca5-119">None</span></span>

## <span data-ttu-id="f8ca5-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8ca5-120">OUTPUTS</span></span>

### <span data-ttu-id="f8ca5-121">Microsoft. Azure. Commands. profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="f8ca5-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="f8ca5-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8ca5-122">NOTES</span></span>

## <span data-ttu-id="f8ca5-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8ca5-123">RELATED LINKS</span></span>
