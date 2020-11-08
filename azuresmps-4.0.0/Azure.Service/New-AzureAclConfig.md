---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055201"
---
# <span data-ttu-id="c8f59-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c8f59-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="c8f59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8f59-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f59-103">Tworzy pusty obiekt konfiguracji listy ACL.</span><span class="sxs-lookup"><span data-stu-id="c8f59-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="c8f59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8f59-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8f59-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8f59-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f59-106">Polecenie cmdlet **New-AzureAclConfig** umożliwia utworzenie pustego obiektu konfiguracji listy kontroli dostępu (ACL).</span><span class="sxs-lookup"><span data-stu-id="c8f59-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="c8f59-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8f59-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f59-108">Przykład 1. Tworzenie obiektu konfiguracji ACL</span><span class="sxs-lookup"><span data-stu-id="c8f59-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="c8f59-109">To polecenie tworzy pusty obiekt konfiguracji listy ACL, a następnie zapisuje go w zmiennej $Acl.</span><span class="sxs-lookup"><span data-stu-id="c8f59-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="c8f59-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8f59-110">PARAMETERS</span></span>

### <span data-ttu-id="c8f59-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8f59-111">-InformationAction</span></span>
<span data-ttu-id="c8f59-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c8f59-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8f59-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c8f59-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8f59-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c8f59-114">Continue</span></span>
- <span data-ttu-id="c8f59-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c8f59-115">Ignore</span></span>
- <span data-ttu-id="c8f59-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="c8f59-116">Inquire</span></span>
- <span data-ttu-id="c8f59-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8f59-117">SilentlyContinue</span></span>
- <span data-ttu-id="c8f59-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c8f59-118">Stop</span></span>
- <span data-ttu-id="c8f59-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c8f59-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f59-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8f59-120">-InformationVariable</span></span>
<span data-ttu-id="c8f59-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c8f59-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f59-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f59-122">CommonParameters</span></span>
<span data-ttu-id="c8f59-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f59-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f59-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f59-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f59-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8f59-125">INPUTS</span></span>

## <span data-ttu-id="c8f59-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8f59-126">OUTPUTS</span></span>

## <span data-ttu-id="c8f59-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8f59-127">NOTES</span></span>

## <span data-ttu-id="c8f59-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8f59-128">RELATED LINKS</span></span>

[<span data-ttu-id="c8f59-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c8f59-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="c8f59-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c8f59-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="c8f59-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c8f59-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


