---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054954"
---
# <span data-ttu-id="f67a7-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="f67a7-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="f67a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f67a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f67a7-103">Tworzy obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="f67a7-103">Creates a namespace.</span></span>

## <span data-ttu-id="f67a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f67a7-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f67a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f67a7-105">DESCRIPTION</span></span>
<span data-ttu-id="f67a7-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f67a7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f67a7-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f67a7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f67a7-108">Polecenie cmdlet **New-AzureSBNamespace** tworzy obszar nazw usługi do użytku z usługą Service Bus na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f67a7-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="f67a7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f67a7-109">EXAMPLES</span></span>

### <span data-ttu-id="f67a7-110">Przykład 1. tworzenie przestrzeni nazw usługi</span><span class="sxs-lookup"><span data-stu-id="f67a7-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="f67a7-111">Przykłady Tworzenie obszaru nazw usługi do użytku z usługą Service Bus na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f67a7-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="f67a7-112">W obu przykładach znajdują się wymagane wartości parametrów, ale tylko te, które zawierają nazwy parametrów.</span><span class="sxs-lookup"><span data-stu-id="f67a7-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="f67a7-113">Można użyć drugiego przykładu, ponieważ oba parametry są pozycjonowane i ich wartości są podane w wymaganej kolejności.</span><span class="sxs-lookup"><span data-stu-id="f67a7-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="f67a7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f67a7-114">PARAMETERS</span></span>

### <span data-ttu-id="f67a7-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="f67a7-115">-CreateACSNamespace</span></span>
<span data-ttu-id="f67a7-116">Określa, czy oprócz obszaru nazw usługi ma zostać utworzony skojarzony obszar nazw ACS.</span><span class="sxs-lookup"><span data-stu-id="f67a7-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f67a7-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f67a7-117">-Location</span></span>
<span data-ttu-id="f67a7-118">Określa region nowego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f67a7-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="f67a7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f67a7-119">-Name</span></span>
<span data-ttu-id="f67a7-120">Określa nazwę nowego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f67a7-120">Specifies a name for the new namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f67a7-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="f67a7-121">-NamespaceType</span></span>
<span data-ttu-id="f67a7-122">Określ, czy chcesz używać obszaru nazw do obsługi wiadomości, czy koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f67a7-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f67a7-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="f67a7-123">-Profile</span></span>
<span data-ttu-id="f67a7-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f67a7-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f67a7-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f67a7-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f67a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67a7-126">CommonParameters</span></span>
<span data-ttu-id="f67a7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f67a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67a7-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f67a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67a7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f67a7-129">INPUTS</span></span>

## <span data-ttu-id="f67a7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f67a7-130">OUTPUTS</span></span>

## <span data-ttu-id="f67a7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f67a7-131">NOTES</span></span>

## <span data-ttu-id="f67a7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f67a7-132">RELATED LINKS</span></span>

[<span data-ttu-id="f67a7-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="f67a7-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


