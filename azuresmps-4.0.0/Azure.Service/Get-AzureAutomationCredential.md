---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054625"
---
# <span data-ttu-id="0a916-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0a916-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="0a916-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a916-102">SYNOPSIS</span></span>

<span data-ttu-id="0a916-103">Pobiera poświadczenia usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0a916-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="0a916-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a916-104">SYNTAX</span></span>

### <span data-ttu-id="0a916-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a916-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a916-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0a916-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a916-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0a916-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0a916-108">Polecenie cmdlet **Get-AzureAutomationCredential** pobiera co najmniej jedno z poświadczeń usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0a916-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="0a916-109">Domyślnie zwracane są wszystkie poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="0a916-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="0a916-110">Aby uzyskać określone poświadczenie, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="0a916-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="0a916-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a916-111">EXAMPLES</span></span>

### <span data-ttu-id="0a916-112">Przykład 1: pobieranie wszystkich poświadczeń</span><span class="sxs-lookup"><span data-stu-id="0a916-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0a916-113">To polecenie pobiera wszystkie poświadczenia konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0a916-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0a916-114">Przykład 2: uzyskiwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="0a916-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="0a916-115">To polecenie pobiera poświadczenia o nazwie moje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="0a916-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="0a916-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a916-116">PARAMETERS</span></span>

### <span data-ttu-id="0a916-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a916-117">-AutomationAccountName</span></span>
<span data-ttu-id="0a916-118">Określa nazwę konta automatyzacji z poświadczeniami do pobrania.</span><span class="sxs-lookup"><span data-stu-id="0a916-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="0a916-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a916-119">-Name</span></span>
<span data-ttu-id="0a916-120">Określa nazwę poświadczenia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="0a916-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a916-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="0a916-121">-Profile</span></span>
<span data-ttu-id="0a916-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a916-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a916-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0a916-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a916-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a916-124">CommonParameters</span></span>
<span data-ttu-id="0a916-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a916-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a916-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a916-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a916-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a916-127">INPUTS</span></span>

## <span data-ttu-id="0a916-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a916-128">OUTPUTS</span></span>

### <span data-ttu-id="0a916-129">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="0a916-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="0a916-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a916-130">NOTES</span></span>

## <span data-ttu-id="0a916-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a916-131">RELATED LINKS</span></span>

[<span data-ttu-id="0a916-132">Nowe — AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0a916-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="0a916-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0a916-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="0a916-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0a916-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


