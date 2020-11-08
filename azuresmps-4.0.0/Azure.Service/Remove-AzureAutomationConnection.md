---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055458"
---
# <span data-ttu-id="3a702-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3a702-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="3a702-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a702-102">SYNOPSIS</span></span>

<span data-ttu-id="3a702-103">Usuwa połączenie z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3a702-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="3a702-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a702-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a702-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a702-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3a702-106">Polecenie cmdlet **Remove-AzureAutomationConnection** usuwa połączenie z usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3a702-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="3a702-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a702-107">EXAMPLES</span></span>

### <span data-ttu-id="3a702-108">Przykład 1: Usuwanie połączenia</span><span class="sxs-lookup"><span data-stu-id="3a702-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="3a702-109">To polecenie usuwa certyfikat o nazwie "połączenie" na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3a702-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3a702-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a702-110">PARAMETERS</span></span>

### <span data-ttu-id="3a702-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a702-111">-AutomationAccountName</span></span>
<span data-ttu-id="3a702-112">Określa nazwę konta automatyzacji z poświadczeniami.</span><span class="sxs-lookup"><span data-stu-id="3a702-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="3a702-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3a702-113">-Force</span></span>
<span data-ttu-id="3a702-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a702-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a702-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a702-115">-Name</span></span>
<span data-ttu-id="3a702-116">Określa nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="3a702-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="3a702-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="3a702-117">-Profile</span></span>
<span data-ttu-id="3a702-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a702-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a702-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3a702-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a702-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a702-120">CommonParameters</span></span>
<span data-ttu-id="3a702-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a702-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a702-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a702-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a702-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a702-123">INPUTS</span></span>

## <span data-ttu-id="3a702-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a702-124">OUTPUTS</span></span>

## <span data-ttu-id="3a702-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a702-125">NOTES</span></span>

## <span data-ttu-id="3a702-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a702-126">RELATED LINKS</span></span>

[<span data-ttu-id="3a702-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3a702-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="3a702-128">Nowe — AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3a702-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="3a702-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="3a702-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


