---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055450"
---
# <span data-ttu-id="4956b-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="4956b-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="4956b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4956b-102">SYNOPSIS</span></span>

<span data-ttu-id="4956b-103">Usuwa typ połączenia.</span><span class="sxs-lookup"><span data-stu-id="4956b-103">Removes a connection type.</span></span>

## <span data-ttu-id="4956b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4956b-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4956b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4956b-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4956b-106">Polecenie cmdlet **Remove-AzureAutomationConnectionType** usuwa typ połączenia usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4956b-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="4956b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4956b-107">EXAMPLES</span></span>

## <span data-ttu-id="4956b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4956b-108">PARAMETERS</span></span>

### <span data-ttu-id="4956b-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4956b-109">-AutomationAccountName</span></span>
<span data-ttu-id="4956b-110">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4956b-110">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4956b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4956b-111">-Force</span></span>
<span data-ttu-id="4956b-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4956b-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4956b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4956b-113">-Name</span></span>
<span data-ttu-id="4956b-114">Określa nazwę typu połączenia, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="4956b-114">Specifies the name of the connection type to remove.</span></span>

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

### <span data-ttu-id="4956b-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="4956b-115">-Profile</span></span>
<span data-ttu-id="4956b-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4956b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4956b-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4956b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4956b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4956b-118">CommonParameters</span></span>
<span data-ttu-id="4956b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4956b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4956b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4956b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4956b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4956b-121">INPUTS</span></span>

## <span data-ttu-id="4956b-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4956b-122">OUTPUTS</span></span>

## <span data-ttu-id="4956b-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4956b-123">NOTES</span></span>

## <span data-ttu-id="4956b-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4956b-124">RELATED LINKS</span></span>

