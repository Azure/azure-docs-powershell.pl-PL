---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890209"
---
# <span data-ttu-id="5f217-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="5f217-101">Get-AzProfile</span></span>

## <span data-ttu-id="5f217-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f217-102">SYNOPSIS</span></span>
<span data-ttu-id="5f217-103">Pobierz profile usług obsługiwane przez zainstalowane moduły.</span><span class="sxs-lookup"><span data-stu-id="5f217-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="5f217-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f217-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="5f217-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f217-105">DESCRIPTION</span></span>
<span data-ttu-id="5f217-106">Pobierz profile usług obsługiwane przez zainstalowane moduły.</span><span class="sxs-lookup"><span data-stu-id="5f217-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="5f217-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f217-107">EXAMPLES</span></span>

### <span data-ttu-id="5f217-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f217-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="5f217-109">Uzyskiwanie profilu usługi obsługiwanego przez moduł magazynu</span><span class="sxs-lookup"><span data-stu-id="5f217-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="5f217-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f217-110">PARAMETERS</span></span>

### <span data-ttu-id="5f217-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="5f217-111">-ListAvailable</span></span>
<span data-ttu-id="5f217-112">Lista wszystkich profilów usługi obsługiwanych przez zainstalowane moduły</span><span class="sxs-lookup"><span data-stu-id="5f217-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="5f217-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="5f217-113">-ModuleName</span></span>
<span data-ttu-id="5f217-114">Nazwa modułu do sprawdzenia</span><span class="sxs-lookup"><span data-stu-id="5f217-114">The name of the module to check</span></span>

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

### <span data-ttu-id="5f217-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f217-115">CommonParameters</span></span>
<span data-ttu-id="5f217-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f217-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f217-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f217-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f217-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f217-118">INPUTS</span></span>

### <span data-ttu-id="5f217-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5f217-119">None</span></span>

## <span data-ttu-id="5f217-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f217-120">OUTPUTS</span></span>

### <span data-ttu-id="5f217-121">Microsoft. Azure. Commands. profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="5f217-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="5f217-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f217-122">NOTES</span></span>

## <span data-ttu-id="5f217-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f217-123">RELATED LINKS</span></span>
