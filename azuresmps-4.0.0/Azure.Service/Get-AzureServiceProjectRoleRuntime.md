---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054564"
---
# <span data-ttu-id="959d8-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="959d8-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="959d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="959d8-102">SYNOPSIS</span></span>
<span data-ttu-id="959d8-103">Pobierz środowiska uruchomieniowe dostępne do zainstalowania w roli.</span><span class="sxs-lookup"><span data-stu-id="959d8-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="959d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="959d8-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="959d8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="959d8-105">DESCRIPTION</span></span>
<span data-ttu-id="959d8-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="959d8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="959d8-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="959d8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="959d8-108">Pobiera środowiska uruchomieniowe dostępne do zainstalowania w roli.</span><span class="sxs-lookup"><span data-stu-id="959d8-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="959d8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="959d8-109">EXAMPLES</span></span>

## <span data-ttu-id="959d8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="959d8-110">PARAMETERS</span></span>

### <span data-ttu-id="959d8-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="959d8-111">-Profile</span></span>
<span data-ttu-id="959d8-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="959d8-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="959d8-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="959d8-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="959d8-114">-Runtime</span><span class="sxs-lookup"><span data-stu-id="959d8-114">-Runtime</span></span>
<span data-ttu-id="959d8-115">Nazwa środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="959d8-115">The name of the runtime.</span></span>
<span data-ttu-id="959d8-116">Jeśli określono środowisko uruchomieniowe, zostaną zwrócone tylko określone wersje tego środowiska wykonawczego dostępne do zainstalowania w roli w systemie Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="959d8-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="959d8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="959d8-117">CommonParameters</span></span>
<span data-ttu-id="959d8-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="959d8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="959d8-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="959d8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="959d8-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="959d8-120">INPUTS</span></span>

## <span data-ttu-id="959d8-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="959d8-121">OUTPUTS</span></span>

## <span data-ttu-id="959d8-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="959d8-122">NOTES</span></span>

## <span data-ttu-id="959d8-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="959d8-123">RELATED LINKS</span></span>

[<span data-ttu-id="959d8-124">Dodaj-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="959d8-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="959d8-125">Dodaj-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="959d8-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="959d8-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="959d8-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="959d8-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="959d8-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


